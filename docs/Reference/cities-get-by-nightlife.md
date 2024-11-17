---
layout: page
---

# Get cities by `nightlife` rating

Returns an array of [`cities`](cities.md) objects that contain a specified `nightlife` parameter.

## URL

```shell

{base_url}/cities?nightlife=
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `nightlife` | number | The nightlife rating from 1-10 |

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
    "affordability": "7",
    "nightlife": "10",
    "id": 2
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
| 201 | Created | Requested data created successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
