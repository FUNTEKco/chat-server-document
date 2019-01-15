# Delete a Room
### path
/rooms/:id

### Method
DELETE

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### Path Parameters

| Name        | Description |
| ----------- | ----------- |
| :id         | Room ID     |

```
DELETE /rooms/test-room-123 HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.1.1 (Macintosh; OS X/10.12.5) GCDHTTPRequest
Content-Length: 2

```

### Response Result
Created Room data

```json
{
  "RC": 0,
  "RM": "OK",
  "result": { /* Debugging detail */
    "n": 1,
    "ok": 1
  }
}
```