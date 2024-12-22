---
layout: page
---

# Get all users

Returns an array of [user](users.md) objects from every user in the service.

## Request

```shell

{base_url}/users
```

## Request headers

None

## Request body

None

## Sample return

```js
[
  {
    "name": "Kathy Barnes",
    "location": "Los Angeles",
    "city_visited": "Split, Seattle, New York",
    "city_to_visit": "Tokyo, Sydney, Barcelona",
    "id": 1
  },
  {
    "name": "Rex Fieldman",
    "location": "Las Vegas",
    "city_visited": "Galway, London, Austin",
    "city_to_visit": "Delhi, Johannesburg, Paris",
    "id": 2
  },
  {
    "name": "Ida McHugh",
    "location": "Kansas City",
    "city_visited": "Zurich, Berlin, Milan",
    "city_to_visit": "Rome, Boston, Reykjavik",
    "id": 3
  },
  {
    "name": "Chris O'Brien",
    "location": "Buffalo",
    "city_visited": "Denver, Miami, Mexico City",
    "city_to_visit": "Bogota, Prague, DC",
    "id": 4
  }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
