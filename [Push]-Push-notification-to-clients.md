# Push notification Client
This API should be used by server side.

### path
/push/push2clients

### Method
POST

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | API    Key   |

### Request Body

| Name        | Type   | Description  |
| ----------- | ------ | ------------ |
| clients     | Array  | Array of Client IDs |
| payload     | Object | Object of message |

### Payload
| Name        | Type   | Description  |
| ----------- | ------ | ------------ |
| expiry      | Number | (iOS) Expiry |
| alert       | String | (iOS) Alert  |
| badge       | String | (iOS) Badge  |
| sound       | String | (iOS) Sound  |
| topic       | String | (iOS) Topic  |
| alert       | Object | (iOS) Localization Alert  |
| title       | String | (android) Title |
| collapseKey | String | (android) Collapse Key |
| body        | String | (android) Body |
| icon        | String | (android) Icon url or name |
| type        | String | Notification type |

#### Alert
| Name        | Type   | Description  |
| ----------- | ------ | ------------ |
| loc-key     | String | (iOS) Localization key |
| loc-args    | Array  | (iOS) Localization Args  |


```
POST /push/push2clients HTTP/1.1
API_KEY: 2JYpYhDaQlIQlDSvVLCLLo2MPzFfVm9jYpxw2vuBrmk=
Content-Type: application/json; charset=utf-8
Host: localhost:3100
Connection: close
User-Agent: Paw/3.1.2 (Macintosh; OS X/10.12.6) GCDHTTPRequest
Content-Length: 285

{"clients":["1485248560558"],"payload":{"topic":"io.ubee.agent.ios","badge":"99","sound":"ping.aiff","title":"Title","collapseKey":"collapseKey","body":"message body","icon":"icon-url","type":"sample-type:sample","alert":{"loc-key":"Localization-Key","loc-args":["Localization-Arg"]}}}
```

Device Received GCM Payload
```
{
  'collapseKey': collapseKey,
  'timeToLive': 3600,
  'notification': {
      title: title,
      body: body,
      icon: icon,
      body_loc_key: body_loc_key,
      body_loc_args: [LOCALIZATION ARGS],
      badge: options.badge,
      click_action: 'push_chatroom',
    }
  },
  data: {
    'loc-key': 'Localization-Key',
    'loc-args': [Object],
    type: 'sample-type:sample',
    payload: [Object] 
  }
}
```

Device Received APN Payload
```
{
  encoding: 'utf8',
  payload: {},
  compiled: false,
  aps: 
   { alert: { 'loc-key': 'Localization-Key', 'loc-args': [Object] },
     sound: 'ping.aiff' },
  expiry: 0,
  priority: 10,
  topic: 'io.ubee.agent.ios'
}
```

### Response Result
None
