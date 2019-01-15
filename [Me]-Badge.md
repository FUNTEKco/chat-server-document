# Get user's total badge
### path
/me/badge

### Method
GET

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |


```
GET /me/badge HTTP/1.1
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.16 (Macintosh; OS X/10.11.6) GCDHTTPRequest
```

### Response Result
User's badge count

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "badge": 10
  }
}
```