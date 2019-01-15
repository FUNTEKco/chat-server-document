# Count Room Messages
Count room messages updated or created after a specified timestamp.

### path
/rooms/:id/count

### Method
GET

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### Path Parameters

| Name        | Description |
| ----------- | ----------- |
| :id         | Room ID     |

### URL parameters
| Name          | Description |
| ------------- | ----------- |
| timeInMS      | Count message updated or created after this specified timestamp (Milliseconds since Unix Epoch) |


```
GET /rooms/58871b877390be11d5f1ab30/count?timeInMS=1488429338625 HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.16 (Macintosh; OS X/10.11.6) GCDHTTPRequest
```

### Response Result

| Name        | Description |
| ----------- | ----------- |
| count       | Count of messages updated or created after the specified time |

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "count": 9
  }
}
```