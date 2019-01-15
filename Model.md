## Web API Response And Socket ACK Format
| Field  | Definition    |  Description | 
| ------ | ------------- | ------------ |
| RC     | Response Code | 0=OK<br/>401=Authorization Error<br/>400=Request Error |
| RM     | Error Message |              |
| result | Result Data   |              |

```json
{
  "RC": 0,
  "RM": "OK",
  "result": {
    ...
  }
}
```


## Room
| Property      | Type    | Description      |
| ------------- | ------- | ---------------- |
| _id           | String  | (auto) Room ID   |
| name          | String  | (optional) Room Name |
| cover         | String  | (optional) Room cover image URL |
| description   | String  | Custom room data |
| latestMessage | Message | Latest message   |
| members       | Array   | Array of Client  |
| memberProperties | Array   | Member properties, such as last read, badge |
| unread        | Integer | Unread message count |
| createdTime   | ISO Date | Room creation time   |
| createdTimeMS | Number   | Room creation time in milliseconds since Unix Epoch |
| muted         | Boolean  | Room is muted in this user's preference |
| encrypted     | Boolean  | Is room messages should be encrypted |

```json
{
  "_id": "58871b877390be11d5f1ab30",
  "description": "Sample Description",
  "appID": "SampleApp",
  "name": "Leigh",
  "cover": "http://loremflickr.com/240/240/style?Melyssa",
  "lastMessage": {
    "_id": "58b7b7c4c246bc0b41afb148",
    "message": 1111234,
    "messageType": "text",
    "sender": {
      "_id": "1485248566481",
      "nickname": "Test2",
      "lastLoginTimeMS": 0,
      "id": "1485248566481"
    },
    "messageTime": "2017-03-02T06:12:20.775Z",
    "messageTimeMS": 1488435140775,
    "id": "58b7b7c4c246bc0b41afb148"
  },
  "memberProperties": [
    {
      "role": "admin",
      "badge": 1,
      "lastRead": "58b7b79b0acc250b377357ab",
      "client": "1485248560558"
    },
    {
      "badge": 0,
      "lastRead": "58b7b7c4c246bc0b41afb148",
      "client": "1485248566481"
    },
    {
      "badge": 61,
      "client": "1485250743313"
    }
  ],
  "members": [
    {
      "_id": "1485248560558",
      "nickname": "Test AB",
      "avatarUrl": "http://example.com/avatarUrl",
      "lastLoginTime": "2017-02-15T09:02:35.934Z",
      "lastLoginTimeMS": 1487149355934,
      "id": "1485248560558"
    },
    {
      "_id": "1485248566481",
      "nickname": "Test2",
      "lastLoginTime": "2017-03-02T07:11:40.398Z",
      "lastLoginTimeMS": 1488438700398,
      "id": "1485248566481"
    },
    {
      "_id": "1485250743313",
      "nickname": "Test 3",
      "lastLoginTime": "2017-03-02T07:49:02.870Z",
      "lastLoginTimeMS": 1488440942870,
      "id": "1485250743313"
    }
  ],
  "unread": 1,
  "id": "58871b877390be11d5f1ab30",
  "createdTime": "2017-08-16T04:55:57.281Z",
  "createdTimeMS": 1502859357281,
  "muted": true,
  "encrypted": false
}
```

## Message
| Property      | Type     | Description         |
| ------------- | -------- | ------------------- |
| _id           | String   | (auto) Message ID   |
| room          | String   | Room ID             |
| message       | String   | Text message content |
| sender        | Client   | Sender              |
| messageType   | String   | Custom message type |
| messageTime   | ISO Date | Message sent time   |
| messageTimeMS | Number   | Message sent time in milliseconds since Unix Epoch |
| createdAt     | ISO Date | Message created time   |
| updatedAt     | ISO Date | Message updated time   |
| updatedAtMS   | Number   | Message updated time in milliseconds since Unix Epoch  |
| originalUrl   | String   | (optional) Media URL |
| thumbnailUrl  | String   | (optional) Thumbnail URL |
| width         | Number   | (optional) Image or video width |
| height        | Number   | (optional) Image or video height |
| duration      | Number   | (optional) Video or audio length |
| latitude      | Number   | (optional) Location latitude |
| longitude     | Number   | (optional) Location longitude |
| reply         | Message  | (optional) A Message that this message replies to |
| member        | Client   | Used when added or deleted member |
| sticker       | String   | (optional) Sticker ID |

```json
{
  "_id": "58a2dc9c965d09221ea7bedb",
  "message": "sadf dsfdf",
  "messageType": "text",
  "sender": {
    "_id": "1485248560558",
    "nickname": "Test AB",
    "avatarUrl": "http://example.com/avatarUrl",
    "lastLoginTime": "2017-02-14T10:31:46.745Z",
    "lastLoginTimeMS": 1487068306745,
    "id": "1485248560558"
  },
  "reply": {
    "_id": "589d8fe5dc637422e577be51",
    "message": "af dsgag fdsf",
    "messageType": "text",
    "sender": {
      "_id": "1485248566481",
      "nickname": "Test2",
      "lastLoginTimeMS": 0,
      "id": "1485248566481"
    },
    "messageTime": "2017-02-10T10:03:17.724Z",
    "messageTimeMS": 1486720997724,
    "id": "589d8fe5dc637422e577be51"
  },
  "messageTime": "2017-02-14T10:31:56.006Z",
  "messageTimeMS": 1487068316006,
  "id": "58a2dc9c965d09221ea7bedb"
},
```

## Client
| Property        | Type     | Description         |
| --------------- | -------- | ------------------- |
| _id             | String   | Custom Client ID    |
| nickname        | String   | Client nickname     |
| avatarUrl       | String   | Client avatar URL   |
| address         | Mixed    | Last auth remote address |
| userAgent       | String   | Last auth user agent |
| mute            | Array    | IDs of muted rooms   |
| lastLoginTime   | ISO Date | Last log-in time     |
| lastLoginTimeMS | Number   | Last log-in time in milliseconds since Unix Epoch   |
| publicKey       | String   | Base64 encoded RSA Public Key used to encrypt message sending to the client |

```json
{
  "_id": "1485248560558",
  "email": "test@test.com",
  "nickname": "Test AB",
  "appID": "SampleApp",
  "chatinAt": "2017-01-24T09:02:40.557Z",
  "__v": 0,
  "avatarUrl": "http://example.com/avatarUrl",
  "address": {
    "port": 56216,
    "family": "IPv6",
    "address": "::1"
  },
  "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/56.0.2924.87 Safari/537.36",
  "mute": [
    "58871b877390be11d5f1ab30"
  ],
  "lastLoginTime": "2017-02-14T10:31:46.745Z",
  "lastLoginTimeMS": 1487068306745,
  "publicKey": "...",
  "id": "1485248560558"
}
```

## File
| Property        | Type     | Description         |
| --------------- | -------- | ------------------- |
| _id             | String   | File ID             |
| length          | Number   | File size           |
| chunkSize       | Number   | Mongo GridFS chunk size |
| uploadDate      | Date     | File upload date    |
| uploadDateMS    | Number   | File upload date in milliseconds since unix epoch |
| md5             | String   | File hash checksum  |
| filename        | String   | Filename            |
| mimetype        | String   | File MIME Type      |
| client          | String   | File creator ID     |
| bucketName      | String   | Bucket contains the file |
| extra           | Mixed    | Custom properties |

```json
{
    "_id": "589d45d889833113ffa5f24f",
    "length": 39435,
    "chunkSize": 261120,
    "uploadDate": "2017-02-10T04:47:20.662Z",
    "md5": "d01c6e3e56230571fb84bdc8c8472add",
    "filename": "pitaya-1.jpg",
    "extra": "{"anyProperty": "something", "roomId: "58871b877390be11d5f1ab30"},
    "appID": "SampleApp",
    "mimetype": "image/jpeg",
    "client": "1485248560558",
    "bucketName": "sampleBucket",
    "id": "589d45d889833113ffa5f24f",
    "uploadDateMS": 1486702040662
}
```