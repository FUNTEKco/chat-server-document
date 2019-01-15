Welcome to the imkit-chatserver-v2 wiki!

# Auth for Client

Authorized client is allowed to request Client APIs, such as Room, Me, etc.

### Headers:

| Field         | Description  |
| ------------- | ------------ |
| CLIENT_KEY    | Client Key   |
| Authorization | Client Token |
| IM-Authorization | Client Token, same as Authorization, both works. Use IM-Authorization to avoid conflict with AWS S3  |

# External auth service
https://github.com/imkit/imkit-auth
![](https://github.com/imkit/imkit-auth/raw/master/Auth2.1.png)

# External badge service
https://github.com/imkit/imkit-badge

# Auth for Platform API (deprecated)
### Headers:

| Field         | Description  |
| ------------- | ------------ |
| API_KEY       | Platform API Key|

Note that, platform admin is allowed to request all APIs, including Platform APIs and Client APIs.


# Auth Flow (deprecated)

![](https://github.com/FUNTEKco/imkit-chatserver-v2/blob/develop/screenshots/auth_flow.png)

 1. Client sign-in Consumer's web service
 1. Consumer generate a random <b>token</b> for authorization
 1. Consumer calls bind-token-to-client with the <b>token</b> and <b>Client ID</b>

## IMKit API
 1. The Client use the token to request IMKit APIs

## Socket.IO
 1. The Client emit <b>auth</b> event with the <b>token</b> after connection established.
