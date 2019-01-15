# List and search Clients

## Permission
Platform API

### path
/admin/clients

### Method
GET

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | Platform API Key   |

### URL Params
| Field | Description |
| ----- | ----------- |
| q     | Mongo query syntax |
| limit | Max number of clients in response |

Example
```json
q={"nickname": {"$regex": ".*AB.*"}}
```
```
GET /admin/clients?q=%7B%22nickname%22:%20%7B%22$regex%22:%20%22.*AB.*%22%7D%7D&limit=10 HTTP/1.1
API_KEY: 2JYpYhDaQlIQlDSvVLCLLo2MPzFfVm9jYpxw2vuBrmk=
Host: 104.199.197.188:3100
Connection: close
User-Agent: Paw/3.1.1 (Macintosh; OS X/10.12.5) GCDHTTPRequest
```

### Respnose Result

| Property   | Description            |
| ---------- | ---------------------- |
| totalCount | (int) matched count       |
| data       | (array) Array of matched Rooms |


```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "totalCount": 1,
    "data": [
      {
        "_id": "1485248560558",
        "email": "test@test.com",
        "nickname": "Test AB",
        "avatarUrl": "https://farm2.staticflickr.com/1261/5110834170_0797f39278_z_d.jpg",
        "address": {
          "port": 49315,
          "family": "IPv6",
          "address": "::ffff:118.168.96.151"
        },
        "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_12_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/59.0.3071.115 Safari/537.36",
        "lastLoginTime": "2017-07-09T12:13:08.127Z",
        "lastLoginTimeMS": 1499602388127,
        "id": "1485248560558"
      }
    ]
  }
}
```