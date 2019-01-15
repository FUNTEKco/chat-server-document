Step 1. Configuration

Emit event: conf

Arguments: Data config object

| Key | Value | Description |
| --- | ----- | ----------- |
| encoding | base64 | Enable receiving base64-encoded data from socket server, to avoid socket-io parsing issue |


Step 2. Authorization

Emit event: auth

Arguments: Token, DeviceId

| Argument | Description |
| --- | ----------- |
| token | Client access token |
| deviceId | Device identity |
