https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html

### APNS push format

| Field    | Type   | Description      |
| -------- | ------ | ---------------- |
| alert    | Mixed  | Alert Object     |
| loc-key  | String | Localization Key, in format of im_loc_${MessageType} |
| loc-args | Array  | Localization string formatting arguments <br/> $1=>sender nickname, $2=>Content |


#### Localization keys

```
im_loc_text
im_loc_image
im_loc_video
im_loc_audio
im_loc_sticker
...
```

```json
{
    "aps" : {
        "alert" : {
            "loc-key" : "im_loc_text",
            "loc-args" : [ "Jenna", "How do you do?"]
        },
        "sound" : "chime.aiff"
    }
}
```

### FCM(GCM) Push Format
```javascript
{
    'collapseKey': collapseKey,
    'timeToLive': 3600,
    'notification': {
      title: title,
      body: body,
      icon: icon,
      body_loc_key: 'im_loc_text',
      body_loc_args	: [ "Jenna", "How do you do?"],
      badge: options.badge,
      click_action: 'push_chatroom',
    },
    data: {
      'loc-key': 'im_loc_text',
      'loc-args': [ "Jenna", "How do you do?"],
      'type': type,
      'payload': options.payload || options,
    }
}
```

#### payload
```javascript
{
    payload: msg,
    alert: alert,
    sound: config.apns.sound
}
```