---
layout: page
---

# Get all cities

Returns an array of [city](cities.md) objects from every city in the service.

## Request

```shell
{base_url}/cities
```

## Request headers

None

## Request body

None

## Sample return

```js
[
  {
    "city": "Split",
    "country": "Croatia",
    "affordability": "10",
    "nightlife": "8",
    "id": 1
  },
  {
    "city": "Galway",
    "country": "Ireland",
    "affordability": "7",
    "nightlife": "10",
    "id": 2
  },
  {
    "city": "Zurich",
    "country": "Switzerland",
    "affordability": "4",
    "nightlife": "7",
    "id": 3
  },
  {
    "city": "New Orleans",
    "country": "USA",
    "affordability": "9",
    "nightlife": "10",
    "id": 4
  }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Useful links

* [Check for updates](Updates.md).
* [Contact us](mailto:where-to@example.com).
