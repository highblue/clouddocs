# clouddocs
How to create the image in azure
## Download the f5 image in https://downloads.f5.com
1. select the VIRTUAL EDITION
2. select the Azure-Cloud [images for Azure Cloud]
3. select the version (suggest Best) fit customers needs.
Please refer to the link to confirm the corresponding instances.
Examples: Standard_DSxxx
https://clouddocs.f5.com/cloud/public/v1/shared/azure_instances.html
4. save your tar.gz downloads
5. unzip the file to get the **vhd** image, the size should be more 80 GB.

## Get your BYOL license
please confirm with your vendor.

## Create the Virtual network

## Manually upload the images
https://clouddocs.f5.com/cloud/public/v1/azure/Azure_download.html

## Go to azure china
1. https://portal.azure.cn/
2. Login and create resource group
### Go to **Storage** in the side panel or just search.
1. Create **Storage account**
2. Select the **Location** from the dropdown list, choose China North etc..
3. Select the **Account kind**, choose type other than BlobStorage, such as StorageV2. Otherwise you won't be able to create iamge.

### Go to resource type, Image (Microsoft)
1. Click create
2. Specify Resource group
3. Specify the OS type, Linux.
4. Choose the previously created Storage account in the **Storage blob**
- click the +Container in the new UI
- input the name
- select the public access level from the dropdown list based on your consideration.
5. In the new UI, click Upload.
5. Choose Premium SSD in the Account type.
6. Finish.

## Create the vm to select your newly created image.
