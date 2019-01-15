![](https://github.com/FUNTEKco/imkit-chatserver-v2/blob/develop/screenshots/chat_test.png)

http://HOST_URL/chat-test
(e.g. http://triptime.io:3100/chat-test)

### Steps:
 1. Load page
 1. Fill a valid token on the right sidebar.
 1. Perform "Auth", you will use the input token to auth.
 1. If auth passed, you will receive the client's room list.
 1. Fill the Room ID on the right sidebar.
 1. Any message your sent will filled with the Room ID you input.
 1. Send any message you like.
 1. All online members in the room will receive the message.

###Sample
```javascript
// Auth
socket.emit('auth', $('#token').val(), function(ack) {
  if (ack.RC !== 0) {
    console.error('auth', ack);
  } else {
    console.log('auth', ack);
    loadRooms();
  }
  $('#messages').append($('<li>').text('[ACK][auth] ' + JSON.stringify(ack.result)));
});

// Send message
var message = {};
message['message'] = $('#m').val();
message['room'] = $('#room').val();
socket.emit('chat message', message, function(ack) {
  if (ack && ack.RC !== 0) {
    console.error(ack);
  } else {
    console.log(ack);
  }
});

// Handle receive message event
socket.on('chat message', function(msg){
  $('#messages').append($('<li>').text(JSON.stringify(msg)));
});
```