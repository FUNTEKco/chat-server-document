# Bind Token to Client
This API should be used by server side.

### path
/admin/clients/:client-id/token/:token

### Method
PUT

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | API    Key   |

### Path Parameters

| Name        | Description  |
| ----------- | ------------ |
| :client-id  | Client ID    |

### JSON Request Body
| Name        | Description  |
| ----------- | ------------ |
| :token      | Client access token    |

```
PUT /admin/clients/1485248560558/token/ HTTP/1.1
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
| token | Token |
| client | client |
| expirationDate | Expiration date time |
| expirationDateMS | Expiration date time in milliseconds since Unix Epoch |

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    "token": "fVy7YhqBZqEzNO9LhMmcyA==",
    "client": "1485248560558",
    "expirationDate": "2017-02-06T08:42:58.391Z",
    "expirationDateMS": 1486370578391
  }
}
```