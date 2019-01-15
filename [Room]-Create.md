# Create Room
### path
/rooms/

### Method
POST

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### Post Body
| Field         | Type   | Description          |
| ------------- | ------ | -------------------- |
| _id           | String | (Optional) Custom Room ID |
| name          | String | (Optional) Room name |
| cover         | String | (Optional) Room cover image URL |
| description   | String | (Optional) Text or serialized json data |

```
POST /rooms/ HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.14 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 44

{"name":"Martena","cover":"http://loremflickr.com/240/240/style?Kelly"}
```

### Response Result
Created Room data

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "__v": 0,
    "appID": "SampleApp",
    "_id": "588ef83f2e0f6a3855d8518b",
    "members": [],
    "id": "588ef83f2e0f6a3855d8518b",
    "name": "Martena",
    "cover": "http://loremflickr.com/240/240/style?Kelly",
  }
}
```