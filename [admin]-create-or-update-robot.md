# Create or update a robot
This API should be used by server side.

### path
/admin/robots

### Method
POST

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | API    Key   |

### Request Parameters

| Name        | Description  |
| ----------- | ------------ |
| _id         | Client ID, also Robot ID    |
| nickname    | Nickname     |
| avatarUrl   | Avatar URL   |
| callbackUrl   | Callback URL to receiving robot events  |
| requestHeaders | Mixed Object, Headers to request to callback URL |


```
POST /admin/robots HTTP/1.1
API_KEY: fangho_imkit_0412_2018_001_apikey
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.1.8 (Macintosh; OS X/10.13.6) GCDHTTPRequest
Content-Length: 137

{"_id":"robot001","nickname":"Holly Robot","callbackUrl":"http://localhost:3100/echo","requestHeaders":{"SOME_AUTH_KEY":"test-auth-key"}}
```

### Response Result
Updated robot info

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "_id": "robot001",
    "appID": "SampleApp",
    "client": {
      "_id": "robot001",
      "nickname": "Nell Robot",
      "isRobot": true,
      "lastLoginTime": "2018-12-22T07:00:10.385Z",
      "lastLoginTimeMS": 1545462010385,
      "id": "robot001"
    },
    "__v": 0,
    "callbackUrl": "http://localhost:3100/echo",
    "createdAt": "2018-12-22T05:20:52.622Z",
    "requestHeaders": {
      "SOME_AUTH_KEY": "test-auth-key"
    },
    "updatedAt": "2018-12-22T07:00:10.380Z"
  }
}
```