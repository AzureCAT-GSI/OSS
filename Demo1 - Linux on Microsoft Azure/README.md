#Linux Demos
Included below are step-by-step instructions for 5 demos

##Marketplace Demo
**Demonstrate provisioning Linux VMs using Portal -> Marketplace**

  1. Go to [Azure Portal] (http://portal.azure.com) *(Explain we are going to look at the options available to provision new Linux VMs)*
  2. Click '+' 

  ![Portal New Resource](media/image001.png)

  3. CLick 'Compute' *(Explain availabilily of images from partners with pre-installed software/products)*
  4. Search for 'LAMP' stack (Linux, Apache, MySQL, PHP)
 
  ![Portal Search LAMP](media/image003.png)
  
  5. Select the LAMP image from Bitnami
  
  ![Portal Select VM](media/image005.png)

  6. Explain how easy and user-friendly it is to create a VM usng the image. *(You can stop here or actually demo provisioning the VM depending upon the audience's experience with provisioning a VM from the portal)*
  7. Remove the 'Search' and go back to default 'Compute' detail page.
  8. Scroll down to 'Linux Based' VMs *(Talk about the Linux distros supported by Azure)*
   
  ![Portal Select Linux VM](media/image007.png)  

  9. Select 'CentOS-based 7.0' image from OpenLogic
   
  ![Select CentOS](media/image009.png) 

  10. Showcase the option to provision the VM using 'Classic' or 'Resource Manager' approach
  
  ![Provision VM](media/image011.png) 
  
  11. Explain how easy and user-friendly it is to create a VM using the image. *(You can stop here or actually demo provisioning the VM depending upon the audience's experience with provisioning a VM from the portal)*
  
  ![Select OpenLogic VM](media/image013.png)

  12. Click the 'Container Apps'. *(Explain these are shortlisted images from Docker Hub that are made available via the Azure portal. Once selected the image is provisioned using Docker Compose, which allows to provision the image, install Docker and install the container image for the selected software/product (e.g. redis, mysql etc.)*
  
  ![Container Apps](media/image015.png)

  ##VM Depot Demo
  **Demonstrate provisioning Linux VMs made available from the 'community' at VM Depot**
  
  1. In the ‘Compute’ details pane, scroll down to the ‘VM Depot – Community Images’ section. *(Explain we are going to look at the options available from community)*
  2. Go to https://vmdepot.msopentech.com
  3. Search for 'MEAN' *(Explain how it brings forth the MEAN stack based community images to pick from. Explain about the options available to provision the VM from within the VM Depot. We’ll go deeper with the ‘Deployment Script’ )*
  4. Click 'Deployment Script'
  5. Click 'I Agree' in the popup
  6. Pick the 'Region' from the 'Select Region' drop down
  7. Script to provision VM is displayed *(Explain that we can use 'Azure CLI' to execute the script)*


##Azure CLI Demo
**Demonstrate the usage of Azure CLI for scripting Linux based VMs usage

  



