---
layout: page
---

# WHERE TO Service Quick Start: LET'S GO!<!-- omit in toc -->

The **Where To Service API** is a cloud-based service you can use to find the perfect place to explore based on ratings like affordability and nightlife.  To start using this service, all you need is to user and city data!  
This quick start should take **15 minutes** to complete.

- [What you will learn](#what-you-will-learn)
- [Before you begin](#before-you-begin)
- [Users and Cities](#users-and-cities)
- [Recap](#recap)
- [Learn more](#learn-more)

## What you will learn

- [How to add a user.](#enroll-a-new-user)
- [How to find a city in the service.](#find-a-city)
- [How to add a city.](#add-a-city)

## Before you begin

To sucessfully complete this quick start you will need to set up a test environment. Be sure to complete our [GET READY! tutorial](WhereTo-GetReady.md) before you start this quick start.

## Users and Cities

The **Where To Service API** uses JSON files to create its database. In this tutorial, we will use cURL to `POST` and `GET` our data, but you can use any other REST client, such as Postman to send and receive data.

### Enroll a new user

Enrolling a new user in the service requires that you add `POST` the details of a new [`user`](api/user.md) resource to the service. To add a user, you will need to supply the following values:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | user name |
| `location` | string | user location. The location must be in the cities resource. |
| `city_visited` | string | cities visited by the user. The city must be in the cities resource. |
| `city_to_visit` | string | cities the user would like to visit|
| `id` | number | The user's unique record ID |

To enroll a new user:

1. If the Where To service is not running, start it by using this command in your command-line tool.

    ```shell
    cd <your-github-workspace>/WHERE-TO-2024/api 
    sh start-server.sh
    ```

2. Open another command-line window.
3. To create a new user resource, in the new command-line window, enter this curl command:

    ```shell
    curl -X POST http://localhost:3000/users \
    > -H "Content-Type: application/json" \
    > -d '{"name": "Liza Dee", "location": "Porto", "city_visited": "Bangkok, Delhi, Boston", "city_to_visit": "Quito, Sydney, Tokyo"}'
    ```

4. The curl command should display a response body like this with the user name you supplied. The response should also include a new user `id`.

    ```js
    {
        "name": "Liza Dee",
        "location": "Porto",
        "city_visited": "Bangkok, Delhi, Boston",
        "city_to_visit": "Quito, Sydney, Tokyo",
        "id": 5
    }
    ```

    - If the user's `location` is not in the `cities` resource, you will need to add it.
    - If the user includes a city in the `city_visited` parameter that is not in the `cities` resource, you will need to add it.
    - Currently, you must search the resource to confirm if a city is or is not in the resource.

### Find a city

Now we'll see if our new user's `location` value is already in the service.

1. Add the value of the new user's `location` as the value of the `name` parameter. In this example, the value of the  `location` is `Porto`.

   ```shell
    curl http://localhost:3000/cities?name=Porto
    ```

2. If the curl command returns an empty curly braces `{}`, then you need to add the location to the city resource.
3. Use the same method to check if the cities listed in the `city_visited` parameter are present.

### Add a city

To add a new city to the service, we use a `POST` command that's similar to what we just used to create the `user` record. The difference is that now we need to supply the following data.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `city` | string | City name |
| `country` | string | The country where the city is location |
| `affordability` | number | The rating for affordability from 1-10|
| `nightlife` | number | The nightlife rating from 1-10 |

1. We'll use the `POST` command in our command-line tool to add the city of **Porto** to the service.

    ```shell
        curl -X POST http://localhost:3000/cities \
        > -H "Content-Type: application/json" \
        > -d '{"city": "Porto", "country": "Portugal", "affordability": "7", "nightlife": "10"}'
    ```

2. The curl command should return something like this with a new city `id`.

    ```shell
    {
        "city": "Porto",
        "country": "Portugal",
        "affordability": "7",
        "nightlife": "10",
        "id": 6
    }
     ```

3. Now add any of the user's `cities_visited` cities that are not already in the service.

## Recap

**Congratulations!!** You've successfully created a new user and added some cities that weren't in the service. You also queried the To-Do service to learn if a city was or was not in the service. To learn more about what else is possible, we invite you to take a look at some of our other tutorials.

## Learn more

- [Find a city by its nightlife rating](../Reference/cities-get-by-nightlife.md)
- [Update the cities visited value](../Reference/users-update-city_visited-city_to_visit-by-user_name.md)
