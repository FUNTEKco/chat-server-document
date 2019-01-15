# Create or update a client
This API should be used by server side.

### path
/admin/clients

### Method
POST

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | API    Key   |

### Request Parameters

| Name        | Description  |
| ----------- | ------------ |
| _id         | Client ID    |
| Any custom object, for example |
| nickname    | Nickname     |
| avatarUrl   | Avatar URL   |


```
POST /admin/clients HTTP/1.1
API_KEY: 2JYpYhDaQlIQlDSvVLCLLo2MPzFfVm9jYpxw2vuBrmk=
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Content-Type: application/json; charset=utf-8
Host: 104.199.197.188:3100
Connection: close
User-Agent: Paw/3.0.16 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 111

{"email":"test@test.com","nickname":"Test AB","_id":"1485248560558","avatarUrl":"http://example.com/avatarUrl"}

```

### Response Result
Updated client info

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
      "port": 57471,
      "family": "IPv6",
      "address": "::1"
    },
    "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/56.0.2924.87 Safari/537.36",
    "mute": [],
    "lastLoginTime": "2017-02-15T09:02:35.934Z",
    "lastLoginTimeMS": 1487149355934,
    "id": "1485248560558"
  }
}
```