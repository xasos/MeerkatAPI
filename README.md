# MeerkatAPI

Unofficial API Documentation for [Meerkat](http://meerkatapp.co), mostly sniffed through Charles Proxy.

**Notice**: Not complete, under active development.

## Endpoints

Grouped by Base URL, since Meerkat hosts different components of their API on different sub-domains. 

- `GET /broadcasts`

### [Follows](/v3_resources/follows.md)

| Endpoint | Description |
| ---- | --------------- |
| [GET /channels/:channel/follows](/v3_resources/follows.md#get-channelschannelfollows) | Get channel's list of following users |
| [GET /users/:user/follows/channels](/v3_resources/follows.md#get-usersuserfollowschannels) | Get a user's list of followed channels |
| [GET /users/:user/follows/channels/:target](/v3_resources/follows.md#get-usersuserfollowschannelstarget) | Get status of follow relationship between user and target channel |
| [PUT /users/:user/follows/channels/:target](/v3_resources/follows.md#put-usersuserfollowschannelstarget) | Follow a channel |
| [DELETE /users/:user/follows/channels/:target](/v3_resources/follows.md#delete-usersuserfollowschannelstarget) | Unfollow a channel |


## License
[MIT License](LICENSE)
