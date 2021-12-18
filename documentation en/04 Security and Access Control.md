# Security and Access Control

## Access control levels

DocumentHub offers 3 levels of access control:
- **Library level access control**
- **Catalog level access control**
- **Document level access control**


## Authorization

There are 2 type of authorization:
- **Basic authorization** when you access DocumentHub content from your backend application and you send the library ID and secret
- **Bearer authorization** when you access DocuemntHub content directly from your frontend application and in this case you send the bearer token (JWT)

## SSO

**DocumentHub SSO component** can be used for a quick integration with IBM SSO or you can use your own login mechanism.

**DocumentHub JavaScript package** can handle the complete SSO, token and cookie process automatically with just one line of code: ```documenthub.ensureIBMidLogin('demo')```

