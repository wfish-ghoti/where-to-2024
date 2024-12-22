---
layout: page
---

# Update User Travel History and Add New Cities to Visit

After a user visits a city, update their details by adding that city to the `city_visited` parameter and removing it (if necessary) from the `city_to_visit` parameter. At the same time, you can add more cities to explore to the `city_to_visit` parameter.

This simple tutorial will show you how and should only take **5 minutes** to complete.

## Before you begin

To sucessfully complete this tutorial you will need to set up a test environment. Be sure to complete our [GET READY! tutorial](WhereTo-GetReady.md) before you start this quick start.

## Begin the tutorial

*Chris O'Brien (user id #4) has finally taken his dream vacation to Prague! Ever the travel bug, he's already thinking of his next trip to Tokyo.*

In this tutorial, we'll update his information to reflect this.

1. If the Where To service is not running, start it by using this command in your command-line tool.

    ```shell
    cd <your-github-workspace>/WHERE-TO-2024/api 
    sh start-server.sh
    ```

2. Open another command-line window.
3. Use the following curl command `id` to call up the user's entry in the database.

    ```shell
      curl http://localhost:3000/users?id=4
    ```

    The system responds with Chris's current entry in the database.

    ```js
      [
        {
          "name": "Chris O'Brien",
          "location": "Buffalo",
          "city_visited": "Denver, Miami, Mexico City",
          "city_to_visit": "Bogota, Prague, DC",
          "id": 4
        }
      ]
    ```

4. Now we will use the `PATCH` command in our command-line tool to add **Prague** to the `city_visited` parameter and remove it from the `city_to_visit` parameter.

    At the same time, we will add **Tokyo** to the `city_to_visit` parameter.

    ```shell
    curl -X PATCH http://localhost:3000/users/4 \
    > -H "Content-Type: application/json" \
    > -d '{"city_visited": "Denver, Miami, Mexico City, Prague", "city_to_visit": "Bogota, DC, Tokyo"}'
    ```

    The system responds with an updated entry.

    ```js
      [
        {
          "name": "Chris O'Brien",
          "location": "Buffalo",
          "city_visited": "Denver, Miami, Mexico City, Prague",
          "city_to_visit": "Bogota, DC, Tokyo",
          "id": 4
        }
      ]
    ```

## Recap

**Congratulations!!** You've successfully updated a user's details to reflect their travel history and future. Now it's time for Chris to add and rate Prague in the `cities` resource.

## Learn more

- [Add a city](../Reference/cities-add-city.md)
