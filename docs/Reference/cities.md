---
layout: page
---

# `cities` resource

Base endpoint:

```shell

{server_url}/cities
```

Contains information about the cities entered into the service.

A city must be in the cities resource to be available to the `city_visited` and the `location` property in the users resource. Learn more about the [users resource](users.md).

## Resource properties

Sample `cities` resource

```js

  {
    "city": "Split",
    "country": "Croatia",
    "affordability": 10,
    "nightlife": 8,
    "cuisine": 9,
    "safety": 8,
    "id": 1
  },
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `city` | string | City name |
| `country` | string | The country where the city is location |
| `affordability` | number | How affordable is this city? Rated from 1-10|
| `nightlife` | number | How vibrant is the nightlife of the city? Rated from 1-10 |
| `cuisine` | number | The food scene: restaurants, street food, farmer's markets. Rated from 1-10 |
| `safety` | number | How safe is the city? Rated from 1-10 |
| `id` | number | The city's unique record ID |

## READ

* [Get all cities](cities-get-all-cities.md)
* [Get cities by nightlife](cities-get-by-nightlife.md)
* [Add a city](cities-add-city.md)
* [List of references](../referencetopics.md)
