# Get User Info
### path
/me

### Method
GET

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |


```
GET /me HTTP/1.1
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Host: 104.199.197.188:3100
Connection: close
User-Agent: Paw/3.0.15 (Macintosh; OS X/10.11.6) GCDHTTPRequest

```

### Response Result
Client Info

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "_id": "1485248560558",
    "email": "test@test.com",
    "nickname": "Test CCDD",
    "appID": "SampleApp",
    "chatinAt": "2017-01-24T09:02:40.557Z",
    "__v": 0,
    "avatarUrl": "http://example.com/avatarUrl",
    "address": {
      "port": 52808,
      "family": "IPv6",
      "address": "::ffff:210.242.193.226"
    },
    "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/55.0.2883.95 Safari/537.36",
    "lastLoginTime": "2017-02-02T09:20:36.514Z",
    "lastLoginTimeMS": 1486027236514,
    "id": "1485248560558"
  }
}
```