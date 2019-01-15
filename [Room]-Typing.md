# Send a Typing event to room

### path

/rooms/:roomId/typing

| Field         | Description  |
| ------------- | ------------ |
| roomId        | Room ID   |

### Method
POST

### Headers:

#### For client

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |


### Post Body
#### Message
| Field         | Type   | Description          |
| ------------- | ------ | -------------------- |
| message       | String | Typing content       |

```
POST /rooms/demo-room/typing HTTP/1.1
CLIENT_KEY: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhcGlLZXkiOiIySllwWWhEYVFsSVFsRFN2VkxDTExvMk1QekZmVm05allweHcydnVCcm1rPSIsImNyZWF0ZUF0IjoxNDk5NTc3MjgzMDUwLCJjbGllbnRJZCI6IjliZWQ2ZmRhLThjNTItNGE0My04OWI4LTJjMzdiZmVkMjQ2ZCJ9.bmXdn-rWmHqgX57AH2t7EfNJrm88MEVDO1t7sQTKo74
Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6InRlc3QtdXNlciIsIm5pY2tuYW1lIjoiU2hlbGxleSIsImF2YXRhclVybCI6Imh0dHBzOi8vZ2xvYmFsYXNzZXRzLnN0YXJidWNrcy5jb20vYXNzZXRzL2MxZjRjZDAyZGUyNDQ4M2ViODZjNjk2NDAxYWQ0MjEzLmpwZyIsImV4cCI6MTUyNjAwOTAyNiwiaWF0IjoxNTI1OTIyNjI2fQ.-o6Mdp-QVjKWiJe5tZP1atzbE7RPsDMPlvmTuO_GRsk
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.1.6 (Macintosh; OS X/10.13.4) GCDHTTPRequest
Content-Length: 23

{"message":"Bonjour 2"}

```

### Response Result
Typing event data

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "message": "Bonjour 2",
    "room": "demo-room",
    "sender": "test-user"
  }
}
```