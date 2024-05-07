## Url Shortening:
- urls should be at most "domain.com"/{7 characters} long
- urls can be set to expire
- urls can be created by user per his/her choice
- allow users to opt for getting notifications when someone uses their shortened link

## Redirection:
- urls can require authentication before redirection
- notifications for shortened urls being used should be sent during this
- should be fast as can be

## Custom Alias:
- users can create their own alias for the URL shortening
- users should be able to use their own domain names for shortening
- this alias must be at most 7 characters in length
- alias should be unique

## Analytics:
- keep track of the following metrics:
	- most visited urls
	- no. of visits per url
	- demographics of visits
	- demographics of users (shorteners)
	- more in [[Metrics]]
	- device used by visitors to access links


## API:
- there should be API for frontend of the platform
- there should be API for third party integration
- API should be documented using swagger(for frontend) and redoc(for backend)


## Authentication and Authorization:
- auth methods allowed:
	- username and password
	- oauth(google and Microsoft)
- authentication and authorization should be available for urls through personas
- users should be able to create custom authorization pages for URL redirects
- users an authorize url access based on demographics
### Personas:
- personas are authentication identities created by users.
- These identities can be granted access to certain locations on the platform or can be granted access to urls.
- the activities of personas should be monitored and any activities performed should trigger a notification