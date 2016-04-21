# Year long goals
- Create a cross platform application (Android and Web)
- Create an open source project
- Contribute to an open source project
- Continue and improve personal blog

# This week
- [x] Setup xbox sidekick bitbucket organization
- [x] Write ruby script to get token for xbox live api requests. See [xbox-live-api gem](https://github.com/oakesja/xbox-live-api) for details.
- [x] Create a domain layer project for the xbox sidekick app
- [x] Add getting profile information to the domain layer
- [ ] Add getting xbox one games for a user to the domain layer
- [ ] Add getting xbox 360 games for a user to the domain layer
- [ ] Add getting achievements to the domain layer
- [ ] Setup some type of CI

# Week in review
I decided to create a bitbucket organization for all xbox sidekick code since it allows private repositories for up to 5 users for free.

I started adding fetching profile information to the domain layer. I am still unable to make a request to xbox live to get profile information even though I have authorization header needed. When using the `fetch` api I get the error, `TypeError: The header content contains invalid characters`. When I `encodeURIComponent` to encode the auth header I get a 401 Unauthorized response. I am going to try other HTTP libraries and hopefully they will encode the header properly.

I finally got fetching profile information working!!! The header issue was because the authorization header had a new line character in it.

# Games of the week
- Max Max
