---
layout: page
---

# Get all cities

Returns an array of [city](cities.md) objects that contains all cities that have entered into the service.

## URL

```shell

{base_url}/users
```

## Params

None

## Request headers

None

## Request body

None

## Return body

```js
[
  {
    "city": "Split",
    "country": "Croatia",
    "affordability": 10,
    "nightlife": 8,
    "cuisine": 9,
    "safety": 8,
    "id": 1
  },
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
    "city": "Zurich",
    "country": "Switzerland",
    "affordability": 4,
    "nightlife": 7,
    "cuisine": 7,
    "safety": 9,
    "id": 3
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
    "city": "Los Angeles",
    "country": "USA",
    "affordability": 5,
    "nightlife": 8,
    "cuisine": 8,
    "safety": 7,
    "id": 5
  },
  {
    "city": "Seattle",
    "country": "USA",
    "affordability": 6,
    "nightlife": 7,
    "cuisine": 8,
    "safety": 8,
    "id": 6
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
    "city": "London",
    "country": "Great Britain",
    "affordability": 6,
    "nightlife": 8,
    "cuisine": 6,
    "safety": 7,
    "id": 9
  },
  {
    "city": "Austin",
    "country": "USA",
    "affordability": 7,
    "nightlife": 8,
    "cuisine": 8,
    "safety": 9,
    "id": 10
  },
  {
    "city": "Kansas City",
    "country": "USA",
    "affordability": 9,
    "nightlife": 8,
    "cuisine": 8,
    "safety": 7,
    "id": 11
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
    "city": "Milan",
    "country": "Italy",
    "affordability": 8,
    "nightlife": 8,
    "cuisine": 9,
    "safety": 7,
    "id": 13
  },
  {
    "city": "Denver",
    "country": "USA",
    "affordability": 6,
    "nightlife": 8,
    "cuisine": 7,
    "safety": 9,
    "id": 14
  },
  {
    "city": "Miami",
    "country": "USA",
    "affordability": 7,
    "nightlife": 10,
    "cuisine": 8,
    "safety": 6,
    "id": 15
  },
  {
    "city": "Mexico City",
    "country": "Mexico",
    "affordability": 8,
    "nightlife": 8,
    "cuisine": 10,
    "safety": 7,
    "id": 16
  }
]```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 201 | Created | Requested data created successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
