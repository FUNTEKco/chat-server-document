# Unmute a room

### path
/me/mute/:room

### Method
Delete

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### Path Parameters
| Field         | Description  |
| ------------- | ------------ |
| room          | Room ID      |

```
DELETE /me/mute/58871b877390be11d5f1ab30 HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.15 (Macintosh; OS X/10.11.6) GCDHTTPRequest
```

### Response Result
Updated client data

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "_id": "1485248560558",
    "email": "test@test.com",
    "nickname": "Test AB",
    "appID": "SampleApp",
    "chatinAt": "2017-01-24T09:02:40.557Z",
    "__v": 0,
    "avatarUrl": "http://example.com/avatarUrl",
    "address": {
      "port": 56216,
      "family": "IPv6",
      "address": "::1"
    },
    "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/56.0.2924.87 Safari/537.36",
    "mute": [],
    "lastLoginTime": "2017-02-14T10:31:46.745Z",
    "lastLoginTimeMS": 1487068306745,
    "id": "1485248560558"
  }
}
```