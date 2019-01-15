```javascript
return new gcm.Message({
    'collapseKey': collapseKey,
    'timeToLive': 3600,
    'notification': {
      title: title,
      body: body,
      icon: icon,
      body_loc_key: body_loc_key,
      body_loc_args    : options.alert['loc-args'],
      badge: options.badge,
      click_action: 'push_chatroom',
    },
    data: {
      'loc-key': options.alert['loc-key'],
      'loc-args': options.alert['loc-args'],
      'type': type,
      'payload': options.payload || options,
    }
});
```

body_loc_key = 'im_loc_{MESSAGE_TYPE}'

body_loc_args = ['{SENDER_NICK_NAME}', '{MESSAGE TEXT}']

payload = {Message Model}

type = chatroom_chat:{ROOM_ID}

