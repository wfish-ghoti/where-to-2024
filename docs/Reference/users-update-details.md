---
layout: page
---

# Update user details

Returns updated [`user`](user.md) objects from a specified user id.

## Request

```shell
curl -X PATCH http://localhost:3000/users/{id}
```

## Request headers

-H "Content-Type: application/json"

## Request body

Change the property values, as needed

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | user name |
| `location` | string | user location |
| `city_visited` | string | cities visited by the user. The city must be in the cities resource. |
| `city_to_visit` | string | cities the user would like to visit|

## Sample request

The following sample updates the `city_visited` and `city_to_visit` properties `user id` 5.

```shell
curl -X PATCH http://localhost:3000/users/5 \
> -H "Content-Type: application/json" \
> -d '{"city_visited": "Bangkok, Delhi, Boston, Tokyo", "city_to_visit": "Quito, Sydney, Lima"}'
```

## Sample return

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
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Useful links

* [Check for updates](Updates.md).
* [Contact us](mailto:where-to@example.com).
