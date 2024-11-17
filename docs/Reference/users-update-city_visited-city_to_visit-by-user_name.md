---
layout: page
---

# Update `city_visited` and `city_to_visit` values

Returns updated [`cities`](cities.md) objects that contain a specified `user_name` parameter.

## URL

```shell
curl -X PATCH http://localhost:3000/users/5 \
> -H "Content-Type: application/json" \
> -d '{"city_visited": "Bangkok, Delhi, Boston, Tokyo", "city_to_visit": "Quito, Sydney, Lima"}'
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `city_visited` | string | cities visited by the user. The city must be in the cities resource. |
| `city_to_visit` | string | cities the user would like to visit|

## Request headers

None

## Request body

None

## Return body

```js
[
  {
  "name": "Liza Dee",
  "location": "Porto",
  "city_visited": "Bangkok, Delhi, Boston, Tokyo",
  "city_to_visit": "Quito, Sydney, Lima",
  "id": 5
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
