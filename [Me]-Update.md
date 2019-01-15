# Update User Info
### path
/me

### Method
POST

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |


```
POST /me HTTP/1.1
Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6InRlc3QtdXNlciIsImV4cCI6MTUyNjA5NTkwNywiaWF0IjoxNTI2MDA5NTA3fQ.khnvZHnXdLk-PejwsysWc6LjmpoHCroon9OPlFBBzVQ
CLIENT_KEY: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhcGlLZXkiOiIySllwWWhEYVFsSVFsRFN2VkxDTExvMk1QekZmVm05allweHcydnVCcm1rPSIsImNyZWF0ZUF0IjoxNDk5NTc3MjgzMDUwLCJjbGllbnRJZCI6IjliZWQ2ZmRhLThjNTItNGE0My04OWI4LTJjMzdiZmVkMjQ2ZCJ9.bmXdn-rWmHqgX57AH2t7EfNJrm88MEVDO1t7sQTKo74
Content-Type: application/json; charset=utf-8
Host: 104.199.197.188:3100
Connection: close
User-Agent: Paw/3.1.6 (Macintosh; OS X/10.13.4) GCDHTTPRequest
Content-Length: 23

{"nickname":"Isabelle"}
```

### Response Result
Updated Client Info

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "_id": "test-user",
    "__v": 0,
    "avatarUrl": "https://globalassets.starbucks.com/assets/c1f4cd02de24483eb86c696401ad4213.jpg",
    "nickname": "Isabelle",
    "appID": "SampleApp",
    "mute": [],
    "lastLoginTime": "2018-05-11T03:35:01.656Z",
    "lastLoginTimeMS": 1526009701656,
    "id": "test-user"
  }
}
```