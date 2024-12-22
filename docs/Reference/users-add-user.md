---
layout: page
---

# Add a user

Adds a user object into the service.

## Request

```shell
curl -X POST http://localhost:3000/users
```

## Request header

```shell
-H "Content-Type: application/json"
```

## Request body

Include  `user` resource properties as listed in the [users resource](users.md)

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | user name |
| `location` | string | user location |
| `city_visited` | string | cities visited by the user. The city must be in the cities resource. |
| `city_to_visit` | string | cities the user would like to visit|

## Sample request

```shell
curl -X POST http://localhost:3000/users \
> -H "Content-Type: application/json" \
> -d '{"name": "Liza Dee", "location": "Porto", "city_visited": "Bangkok, Delhi, Boston", "city_to_visit": "Quito, Sydney, Tokyo"}'
```

## Sample return

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
