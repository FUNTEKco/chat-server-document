# Get current socket connection count

## Permission
Platform API

### path
/admin/connection-count

### Method
GET

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | Platform API Key   |


```
GET /admin/connection-count HTTP/1.1
API_KEY: 2JYpYhDaQlIQlDSvVLCLLo2MPzFfVm9jYpxw2vuBrmk=
Host: 104.199.197.188:3100
Connection: close
User-Agent: Paw/3.1.1 (Macintosh; OS X/10.12.5) GCDHTTPRequest
```

### Response Result

| Property   | Description            |
| ---------- | ---------------------- |
| count      | (int) Connection count |

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "count": 10
  }
}
```