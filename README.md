# Image Lambda

Created by Ryan Emmans

## Summary of Problem Domain

- Create an S3 Bucket with “open” read permissions, so that anyone can see the images/files in their browser.
- A user should be able to upload an image at any size, and update a dictionary of all images that have been uploaded so far.
- When an image is uploaded to your S3 bucket, it should trigger a Lambda function which must:
  - Download a file called “images.json” from the S3 Bucket if it exists.
  - The images.json should be an array of objects, each representing an image.
    - Create an empty array if this file is not present.
  - Create a metadata object describing the image.
    - Name, Size, Type, etc.
  - Append the data for this image to the array.
    - Note: If the image is a duplicate name, update the object in the array, don’t just add it.
  - Upload the images.json file back to the S3 bucket.

## Links

- [images.json](https://ryanemmans-images.s3.us-west-2.amazonaws.com/images.json)
- [JSON Data](https://ryanemmans-images.s3.us-west-2.amazonaws.com/images.json?response-content-disposition=inline&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEEkaCXVzLXdlc3QtMiJIMEYCIQCW9mnjKpJTpHcbsMLYrfnfJsCMtiTCRZM14Sl5tU4iRwIhAIYshODyEVT6M7tatnjmSC2qBXsPrucKgjkkOLZa3ZPwKv8CCPL%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQABoMMTk0NzU4OTg1OTU5Igzr6pIRsh0mwyAT6N8q0wKDHgNConv58AMxzeNOz7yJJ77NmWq%2BVxdf4ZFvZcLzQN4TKm2Krri%2FxxCQ7EoG2oetcIXLxAgd4AGRwm0YBqaEcm3nrbO6U2IgYX2spHLD16cSqiBRc248I1spffciqKuKGWMiO%2BDw81%2FtBsmtrLHbO%2Fk1Klcrkwh5hP3Eep4cGqIFPEtMV9kWVpwCT14I%2BXCm5K6dl7%2FDu%2FpqQwLDKEcDalqY1ZM%2BPFWV6UpkO9EEwxXhwDpDQtfI%2BcINKECtQh7JiDmFInd9YMFGvJOncl67GbsMh2g5sdbDpdoUkvX3kaiHOcIi%2B%2FpWEnSpUXhjFp24tjg4gf%2BFY2gX6rj0D%2FwKwFGXibh4rVNNxZCJNAup6byyUXRlfb%2FNntx34z3uWOg6j7NeGO2ZC8SzKmcjwRS98JPcuJbIPS5xFKkghk%2BBz1udT6SNxywesOmMyohL1pu0t5EwuOqvjAY6sgJfjrMnBb36vHveXluf3sVfsaMchhblenzHgm%2BBSFQ58OKrUHgz9%2FXuQ1KsOMv44lP4Er9FmJnDq3RnQakTzg3A2AggIzr7oOyq2F%2FAeeWUFcVou%2Fwe5AZ9ZNfczR0AXTQ7sSVQyZ5cAvOysFxr8A%2BzJjzAXmlagSlseEDT4%2Fm2iCerrgM13PA%2BZGMQe23HTXTwTsG8%2F%2BwEvuncyf84HQYWNXSf3T7%2Fgyi6baT4cNg9eadv4wndHzm382SjG8Hrle6sBhUKD%2BtRBiuHk0fLrst2qK2xOCVACQWR5B1JYVJ%2FrxATt84jmf8jbmv56%2Bl%2B1myEdi79NrisqlThcbSDl5x0b8ZfPP9YDwrPXVxGHEtXO7Wa5Ups5eCigm7%2B4K7ojG5rzcT6FcG2NmwnZRBG0uIFk88%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20211110T232413Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAS2WEKJDTQC5OLKEF%2F20211110%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Signature=f983c964110fd4f516ec0f5d3e38189ffe6cb20babcdef4b366c3d4032c17e51)
- [Pull Requests](https://github.com/ryanemmans/image-lambda/pulls?q=is%3Apr+is%3Aclosed)
