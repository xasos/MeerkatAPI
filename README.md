# MeerkatAPI

Unofficial API Documentation for the internal [Meerkat](http://meerkatapp.co) API. Most endpoints were discovered through Charles Proxy.

**Notice**: Not complete, under active development.

## Endpoints

Meerkat hosts different components of their API on different sub-domains, so base URLs for resources will differ. 

### Broadcasts

#### Base URL: http://resources.meerkatapp.co/broadcasts/

| Endpoint | Description |
| ---- | --------------- |
| GET / | Get channel's list of following users |
| GET /users/:user/follows/channels | Get a user's list of followed channels |
| GET /users/:user/follows/channels/:target | Get status of follow relationship between user and target channel |
| PUT /users/:user/follows/channels/:target | Follow a channel |
| DELETE /users/:user/follows/channels/:target | Unfollow a channel |

### Users

#### Base URL: http://resources.meerkatapp.co/users/

| Endpoint | Description |
| ---- | --------------- |
| GET / | Get channel's list of following users |
| GET /users/:user/follows/channels | Get a user's list of followed channels |
| GET /users/:user/follows/channels/:target | Get status of follow relationship between user and target channel |
| PUT /users/:user/follows/channels/:target | Follow a channel |
| DELETE /users/:user/follows/channels/:target | Unfollow a channel |

## License
[MIT License](LICENSE)
