---
layout: page
---

# Add a user

Enters a user into the service.

## URL

```shell
curl -X POST http://localhost:3000/users \
```

## Params

Include  `user` resource properties as listed in the [users resource](users.md)

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | user name |
| `location` | string | user location |
| `city_visited` | string | cities visited by the user. The city must be in the cities resource. |
| `city_to_visit` | string | cities the user would like to visit|
| `id` | number | The user's unique record ID |

## Request headers

-H "Content-Type: application/json" \

## Sample request body

-d '{"name": "Liza Dee", "location": "Porto", "city_visited": "Bangkok, Delhi, Boston", "city_to_visit": "Quito, Sydney, Tokyo"}'

## Sample return body

```js
[
{
  "name": "Liza Dee",
  "location": "Porto",
  "city_visited": "Bangkok, Delhi, Boston",
  "city_to_visit": "Quito, Sydney, Tokyo",
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
