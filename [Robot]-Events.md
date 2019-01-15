# Events

## Join Room

```json
{  
   "robotID":"robot001",
   "roomID":"demo-room",
   "event":"JOIN_ROOM",
   "data":{  
      "room":"demo-room",
      "sender":{  
         "_id":"sss",
         "nickname":"Desirae",
         "isRobot":false,
         "lastLoginTimeMS":0,
         "id":"sss"
      },
      "members":[  
         {  
            "_id":"sss",
            "nickname":"Desirae",
            "isRobot":false,
            "lastLoginTimeMS":0,
            "id":"sss"
         }
      ]
   }
}
```

## Add Members

```json
{  
   "robotID":"robot001",
   "roomID":"demo-room",
   "event":"ADD_MEMBERS",
   "data":{  
      "room":"demo-room",
      "sender":{  
         "_id":"sss",
         "nickname":"Desirae",
         "isRobot":false,
         "lastLoginTimeMS":0,
         "id":"sss"
      },
      "members":[  
         {  
            "_id":"robot001",
            "nickname":"Doris Robot",
            "isRobot":true,
            "lastLoginTimeMS":0,
            "id":"robot001"
         }
      ]
   }
}
```

## Delete Members

```json
{  
   "robotID":"robot001",
   "roomID":"demo-room",
   "event":"DELETE_MEMBERS",
   "data":{  
      "room":"demo-room",
      "sender":{  
         "_id":"sss",
         "nickname":"Desirae",
         "isRobot":false,
         "lastLoginTimeMS":0,
         "id":"sss"
      },
      "members":[  
         {  
            "_id":"ccc",
            "nickname":"Aurora",
            "isRobot":false,
            "lastLoginTimeMS":0,
            "id":"ccc"
         }
      ]
   }
}
```

## Message

```json
{  
   "robotID":"robot001",
   "roomID":"demo-room",
   "event":"MESSAGE",
   "data":{  
      "_id":"5c1ddf2d1536bbb6c49f7cfe",
      "message":"Bonjour 2",
      "room":"demo-room",
      "sender":{  
         "_id":"sss",
         "nickname":"Desirae",
         "isRobot":false,
         "avatarUrl":"",
         "description":"description la la #1543989664813",
         "lastLoginTime":"2018-12-05T06:01:06.092Z",
         "lastLoginTimeMS":1543989666092,
         "id":"sss"
      },
      "messageType":"text",
      "appID":"SampleApp",
      "__v":0,
      "messageTime":"2018-12-22T06:52:29.380Z",
      "messageTimeMS":1545461549380,
      "id":"5c1ddf2d1536bbb6c49f7cfe"
   }
}
```