# Get file content
### path
/files/:bucketName/:id

| Field         | Type   | Description          |
| ------------- | ------ | -------------------- |
| :bucketName   | String | Custom bucket name which contains the file |
| :id           | String | File ID |

### Method
Get

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| IM-Authorization | Client Token |


```
GET /files/sampleBucket/589d45d889833113ffa5f24f HTTP/1.1
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.15 (Macintosh; OS X/10.11.6) GCDHTTPRequest
```

### Response Result
File content

#### Head
```head
HTTP/1.1 200 OK
X-Powered-By: Express
x-imkit-ObjectID: 589d64f23df6ea1a6048fdb5
Content-Length: 39435
x-imkit-chunkSize: 261120
x-imkit-uploadDateMS: 1486710002560
x-imkit-uploadDate: Fri Feb 10 2017 15:00:02 GMT+0800 (CST)
x-imkit-md5: d01c6e3e56230571fb84bdc8c8472add
x-imkit-filename: pitaya-1.jpg
x-imkit-extra: {"anyProperty": "something"}
x-imkit-appID: SampleApp
Content-Type: image/jpeg
x-imkit-client: 1485248560558
x-imkit-bucketName: sampleBucket
x-imkit-id: 589d64f23df6ea1a6048fdb5
Date: Fri, 10 Feb 2017 07:02:12 GMT
Connection: close
```