---
layout: page
---

# Get cities by `city`

Returns a city [`cities`](cities.md) object that contain a specified `city` parameter.

    - If the user's `location` is not in the `cities` resource, you will need to add it.
    - If the user includes a city in the `city_visited` parameter that is not in the `cities` resource, you will need to add it.

## URL

```shell

  {base_url}/cities?name=Split

```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `city` | string | City name |

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
