# Unregister device token for Push Notification
### path
/me/unsubscribe

### Method
Post

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### Post Parameters
| Field         | Type  | Description  |
| ------------- | ----- | ------------ |
| type          | String | Device Type, [ios, android, fcm, web] |
| deviceId      | String | Unique device id |

```
POST /me/unsubscribe HTTP/1.1
CLIENT_KEY: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhcGlLZXkiOiIySllwWWhEYVFsSVFsRFN2VkxDTExvMk1QekZmVm05allweHcydnVCcm1rPSIsImNyZWF0ZUF0IjoxNDk5NTc3MjgzMDUwLCJjbGllbnRJZCI6IjliZWQ2ZmRhLThjNTItNGE0My04OWI4LTJjMzdiZmVkMjQ2ZCJ9.bmXdn-rWmHqgX57AH2t7EfNJrm88MEVDO1t7sQTKo74
Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImJvc3NpbmlISyIsImV4cCI6MTUzMDY3NjcxOCwiaWF0IjoxNTMwNTkwMzE4fQ.vvUFVw79QUEvKxJWrNgqF_T2z9-tfwZDc36_LwNRD84
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.1.7 (Macintosh; OS X/10.13.4) GCDHTTPRequest
Content-Length: 39

{"type":"fcm","deviceId":"test-device"}

```

### Response Result
Subscribe result

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "n": 0,
    "ok": 1
  }
}
```