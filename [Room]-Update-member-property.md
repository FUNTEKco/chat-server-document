# Update Custom Member Property
Such as role, last location, score, grade, level, any custom properties.

### path
/rooms/:id/member/:client

### Method
PUT

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### Path Parameters

| Name        | Description |
| ----------- | ----------- |
| :id         | Room ID     |
| :client     | Member ID   |


### Post Parameters
| Name        | Type   | Description          |
| ----------- | ------ | -------------------- |
| property    | String | Member property field name |
| value       | Mixed  | New value            |

```
PUT /rooms/58871b877390be11d5f1ab30/member/1485248560558 HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.16 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 35

{"property":"role","value":"admin"}

```

### Response Result
Update result

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "client": "1485248560558",
    "lastRead": "58fec5ca2837bf2b0da94ace",
    "badge": 0,
    "role": "admin"
  }
}
```