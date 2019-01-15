# Revoke Token from a Client
This API should be used by server side.

### path
/admin/clients/:client-id/token/:token

### Method
DELETE

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | API    Key   |

### Path Parameters

| Name        | Description  |
| ----------- | ------------ |
| :client-id  | Client ID    |

### JSON body request
| Name        | Description  |
| ----------- | ------------ |
| token       | Client access token    |

```
DELETE /admin/clients/1485248560558%7D/token/ HTTP/1.1
API_KEY: 2JYpYhDaQlIQlDSvVLCLLo2MPzFfVm9jYpxw2vuBrmk=
Content-Type: application/json; charset=utf-8
Host: 104.199.197.188:3100
Connection: close
User-Agent: Paw/3.1.5 (Macintosh; OS X/10.13.3) GCDHTTPRequest
Content-Length: 26

{"token":"test-token$123"}

```

### Response Result
| Name | Description |
| ---- | ------------ |

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {}
}
```