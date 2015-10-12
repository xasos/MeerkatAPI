# MeerkatAPI

Unofficial API Documentation for the internal [Meerkat](http://meerkatapp.co) API. Endpoints were discovered through Charles Proxy, and there are more to come.

*Note: This is not an official API. I am not affiliated with Meerkat nor Life on Air, Inc. in any way, and am not responsible for any damage that could be done with it. Use it at your own risk. Any questions, comments, feedback or feature requests should be directed to [xasos](http://github.com/xasos) or via an [issue](https://github.com/xasos/MeerkatAPI/issues) in this repo.*

**NOTICE:** Endpoints not fully complete, under active development.

**Update 05/06/2015** Meerkat has released [documentation](http://developers.meerkatapp.co/) for their API, although it is not as thorough as this documentation

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

### User Information

#### Base URL: http://social.meerkatapp.co/users

| Endpoint | Description |
| ---- | --------------- |
| DELETE /:uid/fans | Get channel's list of following users |
| DELETE /:uid/followers | Get status of follow relationship between user and target channel |
| GET /:uid/followers<sup>*</sup> | Get user's followers |
| GET /:uid/following<sup>*</sup> | Get user's following |
| GET /:uid/profile<sup>*</sup> | Get user's profile |
| GET /i-am-alive<sup>*</sup> | Easter Egg |
| GET /signupSuggested<sup>*</sup> | Signup Suggested |
| OPTIONS /<sup>*</sup> |  |
| OPTIONS /:uid | User id |
| OPTIONS /:uid/followers | Followers |
| OPTIONS /:uid/following | Following |
| OPTIONS /:uid/twitterFriendsSignUp | Twitter from friends |
| OPTIONS /search | Search |
| POST / |  |
| POST /:uid/fans | List of fans |
| POST /:uid/followers | List of followers |
| POST /:uid/invites | Invites |
| POST /:uid/reports | Channel reports |
| POST /:uid/socialLinks | Profile's social links |
| POST /:uid/twitterFriends | "Friends" from Twitter |
| POST /:uid/twitterFriendsSignUp | Sign up with Twitter from friends |
| PUT / |  |
| PUT /:uid | Get user details |
| PUT /:uid/profile | Get profile details |
| PUT /available | Check if user is available |
| PUT /search | Search for users |

## License
[GNU General Public License v3](LICENSE)
