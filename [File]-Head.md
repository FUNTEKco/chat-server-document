# Get HTTP head of a file
### path
/files/:bucketName/:id

| Field         | Type   | Description          |
| ------------- | ------ | -------------------- |
| :bucketName   | String | Custom bucket name which contains the file |
| :id           | String | File ID |

### Method
Head

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |


```
HEAD /files/sampleBucket/58b6734b3f094c17ec29ce48 HTTP/1.1
Authorization: fVy7YhqBZqEzNO9LhMmcyA==
CLIENT_KEY: 9FSk26d4AIbZh0k44F5+DzbetgAJA9WjC7WP36Khm6c=
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.16 (Macintosh; OS X/10.11.6) GCDHTTPRequest
```

### Response Result
HTTP Head of the file

```
HTTP/1.1 200 OK
X-Powered-By: Express
x-imkit-ObjectID: 58b6734b3f094c17ec29ce48
Content-Length: 39435
x-imkit-chunkSize: 261120
x-imkit-uploadDateMS: 1488352075816
x-imkit-uploadDate: Wed Mar 01 2017 15:07:55 GMT+0800 (CST)
x-imkit-md5: d01c6e3e56230571fb84bdc8c8472add
x-imkit-filename: pitaya-1.jpg
x-imkit-extra: {"anyProperty":"something","roomID":"58871b877390be11d5f1ab30"}
x-imkit-appID: SampleApp
Content-Type: image/jpeg
x-imkit-client: 1485248560558
x-imkit-bucketName: sampleBucket
x-imkit-id: 58b6734b3f094c17ec29ce48
Date: Wed, 01 Mar 2017 07:15:29 GMT
Connection: close


```