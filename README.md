# MeerkatAPI

Unofficial API Documentation for the internal [Meerkat](http://meerkatapp.co) API. Endpoints were discovered through Charles Proxy, and there are more to come.

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
| GET /:uid/privateProfile<sup>*</sup> | Get user's private profile |
| GET /:uid/profile<sup>*</sup> | Get user's profile |
| GET /leaderboard | Get top Meerkat users |

Any route with an <sup>*</sup> requires `?v=2` be appended to the end URL.

### User Info

#### Base URL: http://social.meerkatapp.co/users/:uid

Here's a mess of API routes that will be explored soon (all from one domain). Stay tuned!

| Endpoint | Description |
| ---- | --------------- |
| DELETE /:uid/fans | Get channel's list of following users |
| DELETE /:uid/followers | Get status of follow relationship between user and target channel |
| GET /:uid/followers | Follow a channel |
| GET /:uid/following | Unfollow a channel |
| GET /:uid/profile | Unfollow a channel |
| GET /i-am-alive | Unfollow a channel |
| OPTIONS / | Unfollow a channel |
| OPTIONS /:uid | Unfollow a channel |
| OPTIONS /:uid/followers | Unfollow a channel |
| OPTIONS /:uid/following | Unfollow a channel |
| OPTIONS /:uid/twitterFriendsSignUp | Unfollow a channel |
| OPTIONS /search | Unfollow a channel |
| POST / | Unfollow a channel |
| POST /:uid/fans | Unfollow a channel |
| POST /:uid/followers | Unfollow a channel |
| POST /:uid/invites | Unfollow a channel |
| POST /:uid/reports | Unfollow a channel |
| POST /:uid/socialLinks | Unfollow a channel |
| POST /:uid/twitterFriends | Unfollow a channel |
| POST /:uid/twitterFriendsSignUp | Unfollow a channel |
| PUT / | Unfollow a channel |
| PUT /:uid | Unfollow a channel |
| PUT /:uid/profile | Unfollow a channel |
| PUT /available | Unfollow a channel |
| PUT /search | Unfollow a channel |


## License
[GNU General Public License v3](LICENSE)
