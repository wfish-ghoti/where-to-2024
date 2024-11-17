---
layout: page
---

# Add a city

Returns a city entered into the service.

## URL

```shell
curl -X POST http://localhost:3000/cities \
> -H "Content-Type: application/json" \
> -d '{"city": "Dehli", "country": "India", "affordability": "9", "nightlife": "3"}'
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
  "city": "Delhi",
  "country": "India",
  "affordability": "9",
  "nightlife": "3",
  "id": 6
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
