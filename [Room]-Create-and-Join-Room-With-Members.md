# Create and join room with members
### path
/rooms/createAndJoin

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
| invitee       | String or Array | (optional) add member(s) to the created room |

```
POST /rooms/createAndJoin HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.14 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 44

{"name":"Martena","cover":"http://loremflickr.com/240/240/style?Kelly", "invitee": ["aaa","bbb"]}
```

### Response Result
Created Room data

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "_id": "test",
    "name": "Test create and join and invite",
    "cover": "http://loremflickr.com/240/240/style?demo",
    "description": "public demo room",
    "appID": "SampleApp",
    "serviceStatus": 0,
    "createdTime": "2018-10-29T14:14:18.225Z",
    "memberProperties": [],
    "members": [
      {
        "_id": "bossiniHK",
        "nickname": "Willow",
        "lastLoginTime": "2018-10-29T14:14:22.219Z",
        "lastLoginTimeMS": 1540822462219,
        "id": "bossiniHK"
      },
      {
        "_id": "aaa",
        "nickname": "Grace",
        "lastLoginTime": "2018-10-29T14:14:22.219Z",
        "lastLoginTimeMS": 1540822462219,
        "id": "test-device-id"
      },
      {
        "_id": "bbb",
        "nickname": "Qood",
        "lastLoginTime": "2018-10-29T14:14:22.219Z",
        "lastLoginTimeMS": 1540822462219,
        "id": "bbb"
      }
    ],
    "createdTimeMS": 1540822458225,
    "id": "test"
  }
}
```