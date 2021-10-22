# Important updates

## API


### Version 8.0.2

- Search option returnFilterCounters has been added which replicates the filters behaviour on Amazon website and more than that it also adds the live counters expected by the users. See doc: https://developer.ibm.com/edge/documenthub/documentation#searchapi
- Search filter object can contain arrays of conditions, in order to be able to provide multiple conditions on the same field. See doc: https://developer.ibm.com/edge/documenthub/documentation#searchapi
- Filters defined in the catalog.json can have labels. Filter labels will be ignored during the search process. See doc: https://developer.ibm.com/edge/documenthub/documentation#searchapi

### Version 7.1.1

- Search option returnFilterCounters has been added which replicates the filters behaviour on Amazon website and more than that it also adds the live counters expected by the users. See doc: https://developer.ibm.com/edge/documenthub/documentation#searchapi
- Search filter object can contain arrays of conditions, in order to be able to provide multiple conditions on the same field. See doc: https://developer.ibm.com/edge/documenthub/documentation#searchapi
- Filters defined in the catalog.json can have labels. Filter labels will be ignored during the search process. See doc: https://developer.ibm.com/edge/documenthub/documentation#searchapi

### Version 7.1.0

- Create GitHub catalog: POST /catalogs/github - webhook will be automatically added if the EdgeCaaS user has admin access to repository
- Send email from IBM account: POST /email/ibm - a SendGrid account is available for sending emails from IBM accounts. To avoid SPAM, a limit of 100 emails/day is set for each library.


## JavaScript package

### Version 0.0.65
- search function will run an advanced search with a GET request which will execute a bit faster than the advancedSearch function which runs on POST method
- deleteCatalog function has been added

### Version 0.0.52
- 502 status code will be automatically handled by the package by retrying the same request one more time. 
The 502 status codes are returned by the network if the application cannot be reached. They are caused by network issues from the cloud infrastructure.


## Website
