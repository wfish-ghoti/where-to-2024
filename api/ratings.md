---
layout: page
---

# `ratings` resource

Base endpoint:

```shell

{server_url}/ratings
```

Contains information about rating stored for each city in the service.

To have a rating in the service, the city must be added to
the service first. Learn more about the [cities resource](city.md).

## Resource properties

Sample `ratings` resource

```js

{
    // "city_id": 1,
    "city": "Split",
    "affordability": "10",
    "nightlife": "8",
    "cuisine": "9",
    "safety": "8",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `city_id` | number | The ID of the city resource to which this rating is assigned |
| `city` | string | The city name |
| `affordability` | number | The rating for affordability from 1-10|
| `nightlife` | number | The nightlife rating from 1-10 |
| `cuisine` | number | The cuisine rating from 1-10.|
| `safety` | number | The safety rating from 1-10.|
| `id` | number | The task's unique record ID |

<!-- ## READ

* [Get all tasks _(coming soon)_](#resource-properties)
* [Get task by ID _(coming soon)_](#resource-properties)
* [Get task by user ID _(coming soon)_](#resource-properties) -->
