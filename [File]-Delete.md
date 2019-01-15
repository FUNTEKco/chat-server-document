# Delete a file
### path
/files/:bucketName/:id

| Field         | Type   | Description          |
| ------------- | ------ | -------------------- |
| :bucketName   | String | Custom bucket name which contains the file |
| :id           | String | File ID |

### Method
Delete

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |


```
DELETE /files/sampleBucket/58a1774d7f3fc13396e31c40 HTTP/1.1
Authorization: {TOKEN}
CLIENT_KEY: {CLIENT_KEY}
Host: 104.199.197.188:3100
Connection: close
User-Agent: Paw/3.1.2 (Macintosh; OS X/10.12.6) GCDHTTPRequest
```

### Response Result
Execution Result

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "n": 1,
    "ok": 1
  }
}
```