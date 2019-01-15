# Add a client to a room
### path
/rooms/:id/members/:invitee

### Method
Post

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### Path Parameters

| Name        | Description |
| ----------- | ----------- |
| :id         | Room ID     |
| :invitee    | Invitee Client ID  |

```
POST /rooms/58871b877390be11d5f1ab30/members/1485250743313 HTTP/1.1
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.15 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 0
```

### Response Result
Updated Room data.

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "_id": "58871b877390be11d5f1ab30",
    "data": {
      "customProperty": "hello"
    },
    "lastMessage": {
      "_id": "58a2dc9c965d09221ea7bedb",
      "message": "sadf dsfdf",
      "messageType": "text",
      "sender": {
        "_id": "1485248560558",
        "nickname": "Test AB",
        "avatarUrl": "http://example.com/avatarUrl",
        "lastLoginTimeMS": 0,
        "id": "1485248560558"
      },
      "messageTime": "2017-02-14T10:31:56.006Z",
      "messageTimeMS": 1487068316006,
      "id": "58a2dc9c965d09221ea7bedb"
    },
    "lastRead": [
      {
        "message": "58885c9e4d0c89571b777a81",
        "client": "1485248560558"
      }
    ],
    "members": [
      {
        "_id": "1485248560558",
        "nickname": "Test AB",
        "avatarUrl": "http://example.com/avatarUrl",
        "lastLoginTime": "2017-02-14T10:31:46.745Z",
        "lastLoginTimeMS": 1487068306745,
        "id": "1485248560558"
      },
      {
        "_id": "1485248566481",
        "nickname": "Test2",
        "lastLoginTime": "2017-02-10T10:03:13.257Z",
        "lastLoginTimeMS": 1486720993257,
        "id": "1485248566481"
      },
      {
        "_id": "1485250743313",
        "nickname": "Test 3",
        "lastLoginTime": "2017-02-15T03:08:11.658Z",
        "lastLoginTimeMS": 1487128091658,
        "id": "1485250743313"
      }
    ],
    "id": "58871b877390be11d5f1ab30"
  }
}
```