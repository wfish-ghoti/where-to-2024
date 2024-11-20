---
layout: page
---

# Get cities by `nightlife` rating

Returns an array of [`cities`](cities.md) objects that contain a specified `nightlife` parameter.

## URL

```shell

{base_url}/cities?nightlife=10
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `nightlife` | number | How vibrant is the nightlife of the city? Rated from 1-10 |

## Request headers

None

## Request body

None

## Return body

```js
[ 
  {
    "city": "Galway",
    "country": "Ireland",
    "affordability": 7,
    "nightlife": 10,
    "cuisine": 7,
    "safety": 9,
    "id": 2
  },
  {
    "city": "New Orleans",
    "country": "USA",
    "affordability": 9,
    "nightlife": 10,
    "cuisine": 10,
    "safety": 6,
    "id": 4
  },
  {
    "city": "New York",
    "country": "USA",
    "affordability": 3,
    "nightlife": 10,
    "cuisine": 9,
    "safety": 8,
    "id": 7
  },
  {
    "city": "Las Vegas",
    "country": "USA",
    "affordability": 8,
    "nightlife": 10,
    "cuisine": 8,
    "safety": 7,
    "id": 8
  },
  {
    "city": "Berlin",
    "country": "Germany",
    "affordability": 7,
    "nightlife": 10,
    "cuisine": 8,
    "safety": 8,
    "id": 12
  },
  {
    "city": "Miami",
    "country": "USA",
    "affordability": 7,
    "nightlife": 10,
    "cuisine": 8,
    "safety": 6,
    "id": 15
  }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 201 | Created | Requested data created successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
