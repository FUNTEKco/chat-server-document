# Send a Message to room via API.
Not required when sending message via Socket.

### path
/rooms/:roomId/message

| Field         | Description  |
| ------------- | ------------ |
| roomId        | Room ID      |

### Method
POST

### Headers:

#### For client

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

#### For Platform API

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | Platform API Key |

### Post Body
#### Message
| Field         | Type   | Description          |
| ------------- | ------ | -------------------- |
| message       | Any    | Message content      |
| messageType   | String | Custom message type  |
| _id           | String | (Optional), if provided, update the existing message by id |

```
POST /rooms/demo-room/message HTTP/1.1
CLIENT_KEY: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhcGlLZXkiOiIySllwWWhEYVFsSVFsRFN2VkxDTExvMk1QekZmVm05allweHcydnVCcm1rPSIsImNyZWF0ZUF0IjoxNDk5NTc3MjgzMDUwLCJjbGllbnRJZCI6IjliZWQ2ZmRhLThjNTItNGE0My04OWI4LTJjMzdiZmVkMjQ2ZCJ9.bmXdn-rWmHqgX57AH2t7EfNJrm88MEVDO1t7sQTKo74
Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6InRlc3QtdXNlciIsIm5pY2tuYW1lIjoiU2hlbGxleSIsImF2YXRhclVybCI6Imh0dHBzOi8vZ2xvYmFsYXNzZXRzLnN0YXJidWNrcy5jb20vYXNzZXRzL2MxZjRjZDAyZGUyNDQ4M2ViODZjNjk2NDAxYWQ0MjEzLmpwZyIsImV4cCI6MTUyNjAwOTAyNiwiaWF0IjoxNTI1OTIyNjI2fQ.-o6Mdp-QVjKWiJe5tZP1atzbE7RPsDMPlvmTuO_GRsk
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.16 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 83

{"message":"hhhooo","messageType":"announcement"}

```

### Response Result
Sent message data

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "_id": "58bf8f1dc3b24c04d19d9add",
    "room": "58871b877390be11d5f1ab30",
    "message": "hhhooo",
    "messageType": "announcement",
    "sender": null,
    "appID": "SampleApp",
    "__v": 0,
    "messageTime": "2017-03-08T04:57:01.290Z",
    "messageTimeMS": 1488949021290,
    "id": "58bf8f1dc3b24c04d19d9add"
    "updatedAt": "2017-03-08T04:57:01.290Z",
    "updatedAtMS": 1488949021290,
    "createdAt": "2017-03-08T04:57:01.290Z",
  }
}
```