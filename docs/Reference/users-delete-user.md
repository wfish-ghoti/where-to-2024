---
layout: page
---

# Delete a user

Deletes a user registered from the service.

## Request

```shell
curl -X DELETE http://localhost:3000/users/{id} \
```

## Params

| `id` | number | The user's unique record ID |

## Request headers

None

## Sample request

```shell
curl -X DELETE http://localhost:3000/users/5
```

## Sample return

```js
>
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
