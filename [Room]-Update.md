# Update Room
### path
/rooms/:id

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
| Name        | Type   | Description     |
| ----------- | ------ | --------------- |
| name        | String | (Optional) Room name |
| cover       | String | (Optional) Room cover image URL |
| description | String | (Optional) Room description |

```
PUT /rooms/58871b877390be11d5f1ab30 HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.14 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 35

{"description":"Description La La","name":"Martena","cover":"http://loremflickr.com/240/240/style?Kelly"}
```

### Response Result
Updated Room data

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "_id": "58871b877390be11d5f1ab30",
    "name": "Martena",
    "cover": "http://loremflickr.com/240/240/style?Kelly",
    "description": "Description La La",
    "lastMessage": {
      "_id": "588723a346006e17f4d82fe3",
      "message": "hhhooo",
      "messageType": "text",
      "sender": {
        "_id": "1485248560558",
        "nickname": "Test CCDD",
        "avatarUrl": "http://example.com/avatarUrl",
        "lastLoginTimeMS": 0,
        "id": "1485248560558"
      },
      "messageTime": "2017-01-24T09:51:31.375Z",
      "messageTimeMS": 1485251491375,
      "id": "588723a346006e17f4d82fe3"
    },
    "members": [
      {
        "_id": "1485248560558",
        "nickname": "Test CCDD",
        "avatarUrl": "http://example.com/avatarUrl",
        "lastLoginTime": "2017-01-30T08:25:51.552Z",
        "lastLoginTimeMS": 1485764751552,
        "id": "1485248560558"
      }
    ],
    "id": "58871b877390be11d5f1ab30"
  }
}
```