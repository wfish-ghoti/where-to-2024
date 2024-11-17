---
layout: page
---

# Delete a user

Deletes a user registered from the service.

## URL

```shell
curl -X DELETE http://localhost:3000/users/5 \
```

## Params

| `id` | number | The user's unique record ID |

## Request headers

None

## Request body

None

## Return body

```js
>
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 201 | Created | Requested data created successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
