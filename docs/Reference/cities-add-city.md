---
layout: page
---

# Add a city

Adds a city object entered into the service.

## Request

```shell
curl -X POST http://localhost:3000/cities
```

## Request header

```shell
-H "Content-Type: application/json"
```

## Request body

Incldue the `cities` resource properties as listed in the [cities resource](cities.md)

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `city` | string | City name |
| `country` | string | The country where the city is location |
| `affordability` | number | The rating for affordability from 1-10|
| `nightlife` | number | The nightlife rating from 1-10 |

## Sample request

```shell
curl -X POST http://localhost:3000/cities \
> -H "Content-Type: application/json" \
> -d '{"city": "Dehli", "country": "India", "affordability": "9", "nightlife": "3"}'
```

## Sample return

```js
[
{
  "city": "Delhi",
  "country": "India",
  "affordability": "9",
  "nightlife": "3",
  "id": 6
}
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | Requested data created successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Learn more

* [Reference topics](../referencetopics.md#reference-topics)
* [Tutorials](../referencetopics.md#tutorials)

## Useful links

* [Home](../index.md).
* [Check for updates](../Updates.md).
* [Contact us](mailto:where-to@example.com).
