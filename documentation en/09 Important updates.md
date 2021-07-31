# Important updates

## API

### Version 7.1.0

- /catalogs/github (Create GitHub catalog)
  - webhook will be automatically added if the EdgeCaaS user has admin access to repository
- /email/ibm (Send email from IBM account)
  - a SendGrid account is available for sending email from IBM accounts. To avoid SPAM, the limit is set to 100 emails/day for each library.
 
 
## JavaScript package

### Version 0.0.52
- 502 status code will be automatically handled by the package by retrying the same request one more time. 
The 502 status codes are returned by the network if the application cannot be reached. They are caused by network issues from the cloud infrastructure.


## Website
