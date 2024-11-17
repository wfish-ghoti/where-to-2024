---
layout: page
---

# Add a user

Returns a user registered into the service.

## URL

```shell
curl -X POST http://localhost:3000/users \
> -H "Content-Type: application/json" \
> -d '{"name": "Liza Dee", "location": "Porto", "city_visited": "Bangkok, Delhi, Boston", "city_to_visit": "Quito, Sydney, Tokyo"}'
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
