# MeerkatAPI

Unofficial API Documentation for the internal [Meerkat](http://meerkatapp.co) API. Endpoints were discovered through Charles Proxy, and there are more to come.

*Note: This is not an official API. I am not affiliated with Meerkat nor Life on Air, Inc. in any way, and am not responsible for any damage that could be done with it. Use it at your own risk. Any questions, comments, feedback or feature requests should be directed to [xasos](http://github.com/xasos) or via an [issue](https://github.com/xasos/MeerkatAPI/issues) in this repo.*

## Endpoints

Meerkat hosts different components of their API on different sub-domains, so base URLs for resources will differ. 

Any route with a <sup>*</sup> requires `?v=0.1.2` be appended to the end URL. Additionally, some routes require `?auth=xxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx` be appended to the end URL (ideally replacing with your own device auth token).

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

```
{
"result": "rise and shine my child",
"followupActions": {
"stats": "https://stats.meerkatapp.co/logs",
"signIn": "https://social.meerkatapp.co/users/?v=2",
"inviteValidation": "https://social.meerkatapp.co/invite/{inviteCode}?v=2",
"available": "https://social.meerkatapp.co/users/available?v=2",
"signUp": "https://social.meerkatapp.co/users/?v=2"
}
}
```

### User Information

#### Base URL: http://social.meerkatapp.co/users

Here's a mess of API routes that will be explored soon (all from one domain). Stay tuned!

| Endpoint | Description |
| ---- | --------------- |
| DELETE /:uid/fans | Get channel's list of following users |
| DELETE /:uid/followers | Get status of follow relationship between user and target channel |
| GET /:uid/followers<sup>*</sup> | Get user's followers |
| GET /:uid/following<sup>*</sup> | Get user's following |
| GET /:uid/profile<sup>*</sup> | Get user's profile |
| GET /i-am-alive<sup>*</sup> | Easter Egg |
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
