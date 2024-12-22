---
layout: page
---

# `users` resource

Base endpoint:

```shell

{server_url}/users
```

Contains information about the users of the service.

A city must be in the cities resource to be available to the `city_visited` and the `location` property. Learn more about the [cities resource](cities.md).

## Resource properties

Sample `users` resource

```js

{
    "name": "Kathy Barnes",
    "location": "Los Angeles",
    "city_visited": "Split, Seattle, New York",
    "city_to_visit": "Tokyo, Sydney, Barcelona",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | user name |
| `location` | string | user location |
| `city_visited` | string | cities visited by the user. The city must be in the cities resource. |
| `city_to_visit` | string | cities the user would like to visit|
| `id` | number | The user's unique record ID |

## Learn more

* [Reference topics](../referencetopics.md#reference-topics)
* [Tutorials](../referencetopics.md#tutorials)

## Useful links

* [Home](../index.md).
* [Check for updates](../Updates.md).
* [Contact us](mailto:where-to@example.com).
