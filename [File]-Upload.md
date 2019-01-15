# Upload File
### path
/files/:bucketName/

| Field         | Type   | Description          |
| ------------- | ------ | -------------------- |
| bucketName    | String | Custom bucket name   |

### Method
POST Multi-part

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |

### Post Body
| Field         | Type  | Description          |
| ------------- | ----- | -------------------- |
| file          | File  | File to upload       |
| extra         | Mixed | JSON object host custom information |

```
POST /files/sampleBucket/ HTTP/1.1
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Content-Type: multipart/form-data; charset=utf-8; boundary=__X_PAW_BOUNDARY__
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.16 (Macintosh; OS X/10.11.6) GCDHTTPRequest
Content-Length: 39719

--__X_PAW_BOUNDARY__
Content-Disposition: form-data; name="extra"

{"anyProperty": "something", "roomID": "58871b877390be11d5f1ab30"}
--__X_PAW_BOUNDARY__
Content-Disposition: form-data; name="file"; filename="pitaya-1.jpg"
Content-Type: image/jpeg
File Data Part....

### Response Result
File info

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
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
  }
}
```