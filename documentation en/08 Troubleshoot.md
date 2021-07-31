# Troubleshoot

### Image is not accessible on CDN url

If the image is accessible on developer.ibm.com/caas-storage but is not accessible on dw1.s81c.com/caas-storage then it could be because the image contains errors.

CDN tries to optimize the images before caching them into multiple locations around the globe and if an image has errors then the optimization process will fail.

Solution: Fix the image errors and reupload the image to github. Ask support team to flush the CDN cache.
