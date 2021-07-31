# Important updates

## API

### Version 7.1.0

- Create GitHub catalog: POST /catalogs/github - webhook will be automatically added if the EdgeCaaS user has admin access to repository
- Send email from IBM account: POST /email/ibm - a SendGrid account is available for sending emails from IBM accounts. To avoid SPAM, a limit of 100 emails/day is set for each library.
 
 
## JavaScript package

### Version 0.0.52
- 502 status code will be automatically handled by the package by retrying the same request one more time. 
The 502 status codes are returned by the network if the application cannot be reached. They are caused by network issues from the cloud infrastructure.


## Website
