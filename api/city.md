---
layout: page
---

# `cities` resource

Base endpoint:

```shell

{server_url}/cities
```

Contains information about the cities entered into the service.

To have a rating in the service, the city must be added to
the service first. Learn more about the [ratings resource](ratings.md).

## Resource properties

Sample `cities` resource

```js

{
    "city": "Split",
    "country": "Croatia",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `city` | string | City name |
| `country` | string | The country where the city is location |
| `id` | number | The user's unique record ID |

<!-- ## READ

* [Get all cities](users-get-all-users.md)
* [Get users by ID](users-get-user-by-id.md) -->
