# Seach Rooms
### path
/rooms

### Method
GET

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### URL Query Params
| Field | Description |
| ----- | ----------- |
| q     | Mongo query syntax | 
| skip          | Paging offset|
| limit         | Limit of rooms in response |

Example
```json
q={"name": {"$regex": ".*el.*"}}
```
```
GET /rooms?q=%7B%22name%22:%20%7B%22$regex%22:%20%22.*el.*%22%7D%7D&skip=10&limit=50 HTTP/1.1
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
CLIENT_KEY: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhcGlLZXkiOiIySllwWWhEYVFsSVFsRFN2VkxDTExvMk1QekZmVm05allweHcydnVCcm1rPSIsImNyZWF0ZUF0IjoxNDk5NTc3MjgzMDUwLCJjbGllbnRJZCI6IjliZWQ2ZmRhLThjNTItNGE0My04OWI4LTJjMzdiZmVkMjQ2ZCJ9.bmXdn-rWmHqgX57AH2t7EfNJrm88MEVDO1t7sQTKo74
Content-Type: application/x-www-form-urlencoded; charset=utf-8
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
        "_id": "595ef355344d2a63bfd96aaf",
        "name": "Isabelle",
        "cover": "http://loremflickr.com/240/240/style?Maryam",
        "description": "sample description",
        "appID": "SampleApp",
        "memberProperties": [],
        "members": [
          {
            "_id": "1485248566481",
            "nickname": "Test2",
            "avatarUrl": "https://farm5.staticflickr.com/4187/34380436201_fb445103e6_z_d.jpg",
            "lastLoginTime": "2017-06-09T02:46:09.986Z",
            "lastLoginTimeMS": 1496976369986,
            "id": "1485248566481"
          },
          {
            "_id": "1485248560558",
            "nickname": "Test AB",
            "avatarUrl": "https://farm2.staticflickr.com/1261/5110834170_0797f39278_z_d.jpg",
            "lastLoginTime": "2017-07-09T12:13:08.127Z",
            "lastLoginTimeMS": 1499602388127,
            "id": "1485248560558"
          }
        ],
        "unread": 0,
        "id": "595ef355344d2a63bfd96aaf"
      }
    ]
  }
}
```