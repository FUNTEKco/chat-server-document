# Generate Token
Generate a random token

### path
/auth/token

### Method
GET

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | API Key      |

```
GET /auths/token?size=16 HTTP/1.1
API_KEY: 2JYpYhDaQlIQlDSvVLCLLo2MPzFfVm9jYpxw2vuBrmk=
Host: localhost:3100
Connection: close
User-Agent: Paw/3.0.14 (Macintosh; OS X/10.11.6) GCDHTTPRequest

```

### Response

```json
{
  "result": "so5oqIouDLdeTeo5x7CKfA=="
}
```