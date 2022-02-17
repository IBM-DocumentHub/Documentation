# Security and Access Control

Security and access control can take a lot of time for a project:
- develop all the access control code needed in all pages and API endpoints
- test all the possible scenarios
- run external PEN test to confirm there are no backdoors 

DocumentHub offers a simple way to define the security rules and it's already tested by other apps and it's confirmed to be secure and robust.


## Access control levels

DocumentHub offers 3 levels of access control:
- **Library level access control**
- **Catalog level access control**
- **Document level access control**


## Authorization

Authorization is done at the library level. There are 2 types of authorization:
- **Basic authorization** when DocumentHub content is accessed from the backend application and the authorization is done with the library ID and secret
- **Bearer authorization** when DocumentHub content is accessed directly from the frontend application and in the authorization is done with a bearer token (JWT)


## SSO

**DocumentHub SSO component** can be used for a quick integration with IBM SSO or you can use your own login mechanism.

**DocumentHub JavaScript package** can handle the complete SSO, token and cookie process automatically with just one line of code: 

```
documenthub.ensureIBMidLogin('demo')
```

