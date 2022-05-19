# Troubleshoot


## Issues with Libraries

### Changing library secret

Changing library secret can break the production instance. This is similar with changing the database password.

Instead of immediately changing the secret, a safer approach is recommended:
- create a second library
- add the second library to the catalogs, without removing the first library
- test the code in test/staging environment with the second library
- push the code to production and test it again
- remove the first library from the catalogs

Now the code in running in production with the second library id and secret. It's now safe to change the first library secret. Next time you can switch them back, following the same process.


## Issues with Catalogs


### Changes done in GitHub are not reflected in the catalog

**Solutions:**
  - Check if the hook is added to repository: in the repository go to Settings menu then to Hooks tab and see if this hook is added: https://developer.ibm.com/edge/documenthub/api/catalogs/sync
  - Add an email field in the catalog.json to receive email notifications when the catalog sync has errors or warnings: ```"email": "john@ibm.com"```
  - Check when the hook was last started and if it returned any error in the response: click on the hook and scroll down to Recent Deliveries. Click on the first entry from the top and inside it on the Response tab. Check if there is any error returned in the body.
  - Load the catalog by API and check if the field updateError is returned in the catalog JSON



## Issues with Images


### Image is not accessible on CDN url

If the image is accessible on developer.ibm.com/caas-storage but is not accessible on dw1.s81c.com/caas-storage then it could be because the image contains errors.

CDN tries to optimize the images before caching them into multiple locations around the globe and if an image has errors then the optimization process will fail.

**Solution:** Fix the image errors and reupload the image to github. Ask support team to flush the CDN cache.


### Image not accessible after switching catalog from version 7 to version 8

Version 8 uses the catalog id in the attachments path instead of the repository and branch. For security reasons we avoid to expose the repository location.

Version 7 attachments path:
- catalog attachments: https://developer.ibm.com/caas-storage/{gitorg}/{gitrepo}/{gitbranch}/{attachmentsfolder}/{filename}
- document attachments: https://developer.ibm.com/caas-storage/{gitorg}/{gitrepo}/{gitbranch}/{documentid}/{lang}/{attachmentsfolder}/{filename}

Version 8 attachments path:
- catalog attachments: https://developer.ibm.com/caas-storage/{catalogId}/{attachmentsfolder}/{filename}
- document attachments: https://developer.ibm.com/caas-storage/{catalogId}/{documentid}/{lang}/{attachmentsfolder}/{filename}




