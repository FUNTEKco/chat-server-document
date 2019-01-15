# Update Last Read
### path
/rooms/:id/lastRead

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


### Post Parameters
| Name        | Type   | Description          |
| ----------- | ------ | -------------------- |
| message     | String | Last read Message ID |

```
PUT /rooms/58871b877390be11d5f1ab30/lastRead HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.15 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 38

{"message":"58885c9e4d0c89571b777a81"}

```

### Response Result
Update result

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "client": "1485248560558",
    "lastRead": "58b7b79b0acc250b377357ab",
    "badge": 48
  }
}
```

### Socket Event to Room Members
Event: Room
Data
```json
{
  "room": "58871b877390be11d5f1ab30",
  "memberProperty": {
    "client": "1485248560558",
    "lastRead": "58b7b79b0acc250b377357ab",
    "badge": 48
  }
}
```