---
layout: page
---

# `cities` resource

Base endpoint:

```shell

{server_url}/cities
```

Contains information about the cities entered into the service.

A city must be in the cities resource to be available to the `city_visited` property in the users resource. Learn more about the [users resource](users.md).

To have a rating in the service, the city must be added to
the service first. Learn more about the [ratings resource](ratings.md).

## Resource properties

Sample `cities` resource

```js

{
    "city": "Split",
    "country": "Croatia",
    "affordability": "10",
    "nightlife": "8",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `city` | string | City name |
| `country` | string | The country where the city is location |
| `affordability` | number | The rating for affordability from 1-10|
| `nightlife` | number | The nightlife rating from 1-10 |
| `id` | number | The city's unique record ID |

<!-- ## READ

* [Get all cities](users-get-all-users.md)
* [Get users by ID](users-get-user-by-id.md) -->
