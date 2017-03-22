---
permalink: transfer-server-images-between-cloud-regions-with-pitchfork/
audit_date: '2017-03-07'
title: Transfer server images between cloud regions with Pitchfork
type: article
created_date: '2017-02-20'
created_by: Mo Nash
last_modified_date: '2017-03-07'
last_modified_by: Stephanie Fillmon
product: Cloud Images
product_url: cloud-images
---

This article describes how to transfer Rackspace Cloud Servers instance images between regions of the Rackspace Cloud by using [Pitchfork](https://pitchfork.cloudapi.co/). Pitchfork is an interactive Rackspace Cloud API application that simplifies working with the Rackspace Cloud APIs. Using a browser, you can execute any Rackspace API command for any Cloud product without the need to get on a command line or use another CLI tool.

**Note:** You can't transfer images larger than 50 GB, so check the size of the image before you start.

### Getting started

Before you can transfer the images, perform the following steps:

1. Open a new text file. You will be copying information into this file during the following steps.

2. Copy your Rackspace Cloud username and API key, which you'll need to log in to Pitchfork.

   If you don't know your username or API key, use the instructions in [View and reset your API key](/how-to/view-and-reset-your-api-key) to fine them.

3. In Cloud Files, create containers for the image export and the image import:

   - In the same region where the image that you want to transfer currently lives, create a container to export it to, and give the container a descriptive name, such as DFW_IMG_ExportContainer. Then copy the name of the container to the text file.
   
   - In the region to which you want to transfer the image, create a container to import the image to, and give the container a descriptive name, such as ORD_IMG_ImportContainer. Then copy the name of the container to the text file.
   
   For instructions on how to create a container, see [Getting started with Cloud Files and CDN](/how-to/getting-started-with-cloud-files-and-cdn). 

4. Find the image that you want to transfer, and copy that image's UUID to the text file.

   To find the image's UUID, go to the Saved Images section of the Cloud Control Panel, click the name of the image, and copy the ID value (for example, a6da1504-e1c04f40-8461-1ed9a9990e90).
   
You should have five items copied to yoru text file: your Rackspace Cloud username, the API key for that username, the export container name, the import container name, and the UUID of the image that you want to transfer. 

Additionally, we recommend using a third-party application called Cyberduck to download and upload the image. You can, however, use a different open-source (free) application or use the API directly.

### Transfer the image

1. Open a browser and go to https://pitchfork.cloudapi.co/images/#export_task-images.

2. Log in to Pitchfork by clicking the link at the top right of the page and entering your Rackspace Cloud username and API key.

3. From the **Region** list, select the region in which the image currently lives (from which you are exporting it).

4. Export the image to the export container that you created.

   a. In the API Calls list under Tasks, click **Post** for Export Task.
   
   b. For `image_id`, enter the image UUID.
   
   c. For `receiving_container`, enter the name of the export container that you created. 
   
   d. Click **Send API Call**.
   
5. Scroll down to the `request-id` parameter in the Response Body of the call.

   You can use the value of `request-id` to check the status of the export and import from the Get Task Details API call.
   
6. After the image has been exported to the container, download the image to your local host.

   **Tip:** Because of its ease-of-use, we recommend using Cyberduck to download and upload the image.

7. After the image is downloaded, upload it to the import container in the destination region.

8. After the impage is uploaded to the import container, import the image to the destination region:

   a. Go to https://pitchfork.cloudapi.co/images/#import_task-images.
   
   b. In the **Region** list, select the region to which you are transferring the image.
   
   c. For the Import Task call, click **Post**.
   
   d. Enter the name of the image.
   
   e. Enter the import container name and the name of the uploaded image file in the `import_from` field. Do not enter any spaces.
   
   f. Click **Send API Call**.
   
While the API transfers the image from the container to the available images list, you can use the `request_id` value to confirm the progress. If the process is successful, the image is listed and available for use in the destination region.

### Related information

-   [Rackspace Cloud Images API information](https://developer.rackspace.com/docs/cloud-images/v2/developer-guide/)
-   [Cloud Images FAQ](/how-to/cloud-images-faq)
-   [Transferring images between regions of the Rackspace Open Cloud](/how-to/transferring-images-between-regions-of-the-rackspace-open-cloud)
-   [Pitchfork on Github](https://github.com/oldarmyc/pitchfork)
