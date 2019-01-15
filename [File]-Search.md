# Get file metadata
### path
/files/sampleBucket/

| Field         | Type   | Description          |
| ------------- | ------ | -------------------- |
| :bucketName   | String | Custom bucket name which contains the file |


### Method
Get

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### URL Query Parameters
| Field         | Description  |
| ------------- | ------------ |
| q             | Query syntax, such like {"extra.roomID": "58871b877390be11d5f1ab30"} |

```
GET /files/sampleBucket/?q=%7B%22extra.roomID%22:%20%2258871b877390be11d5f1ab30%22%7D HTTP/1.1
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.16 (Macintosh; OS X/10.11.6) GCDHTTPRequest

```

### Response Result
File metadata

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "totalCount": 2,
    "data": [
      {
        "_id": "58b6734b3f094c17ec29ce48",
        "length": 39435,
        "chunkSize": 261120,
        "uploadDate": "2017-03-01T07:07:55.816Z",
        "md5": "d01c6e3e56230571fb84bdc8c8472add",
        "filename": "pitaya-1.jpg",
        "extra": {
          "anyProperty": "something",
          "roomID": "58871b877390be11d5f1ab30"
        },
        "appID": "SampleApp",
        "mimetype": "image/jpeg",
        "client": "1485248560558",
        "bucketName": "sampleBucket",
        "id": "58b6734b3f094c17ec29ce48",
        "uploadDateMS": 1488352075816
      },
      {
        "_id": "58b673463f094c17ec29ce46",
        "length": 39435,
        "chunkSize": 261120,
        "uploadDate": "2017-03-01T07:07:50.876Z",
        "md5": "d01c6e3e56230571fb84bdc8c8472add",
        "filename": "pitaya-1.jpg",
        "extra": {
          "anyProperty": "something",
          "roomID": "58871b877390be11d5f1ab30"
        },
        "appID": "SampleApp",
        "mimetype": "image/jpeg",
        "client": "1485248560558",
        "bucketName": "sampleBucket",
        "id": "58b673463f094c17ec29ce46",
        "uploadDateMS": 1488352070876
      }
    ]
  }
}
```