# MeerkatAPI

Unofficial API Documentation for the internal [Meerkat](http://meerkatapp.co) API. Most endpoints were discovered through Charles Proxy.

**Notice**: Not complete, under active development.

## Endpoints

Meerkat hosts different components of their API on different sub-domains, so base URLs for resources will differ. 

### Broadcasts

#### Base URL: http://resources.meerkatapp.co/broadcasts

| Endpoint | Description |
| ---- | --------------- |
| GET / | Get list of latest broadcasts |
| GET /:broadcastId/activities | Get individual broadcast information |
| GET /:broadcastId/summary | Get individual broadcast information with further action URLs |
| GET /:broadcastId/watchers | Get list and information of watchers |
| GET /:scheduleId/schedule | Get scheduled broadcast information |

### Users

#### Base URL: http://resources.meerkatapp.co/users

| Endpoint | Description |
| ---- | --------------- |
| GET /:uid/privateProfile | Get user's private profile | * Requires
| GET /:uid/profile | Get user's profile |
| GET /leaderboard | Get top Meerkat users |

### User Info

#### Base URL: http://resources.meerkatapp.co/users/:uid/:

```
DELETE /:uid/fans
DELETE /:uid/followers
GET /:uid/followers
GET /:uid/following
GET /:uid/profile
GET /:uid/sweepSessions
GET /i-am-alive
OPTIONS /
OPTIONS /:uid
OPTIONS /:uid/followers
OPTIONS /:uid/following
OPTIONS /:uid/twitterFriendsSignUp
OPTIONS /search
POST /
POST /:uid/fans
POST /:uid/followers
POST /:uid/invites
POST /:uid/reports
POST /:uid/socialLinks
POST /:uid/twitterFriends
POST /:uid/twitterFriendsSignUp
PUT /
PUT /:uid
PUT /:uid/profile
PUT /available
PUT /search
```

| Endpoint | Description |
| ---- | --------------- |
| DELETE /:uid | Get channel's list of following users |
| GET /users/:user/follows/channels | Get a user's list of followed channels |
| GET /users/:user/follows/channels/:target | Get status of follow relationship between user and target channel |
| PUT /users/:user/follows/channels/:target | Follow a channel |
| DELETE /users/:user/follows/channels/:target | Unfollow a channel |

## License
[MIT License](LICENSE)
