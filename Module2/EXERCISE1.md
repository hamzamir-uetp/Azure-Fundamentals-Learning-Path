# Exercise 1: Create an Azure virtual machine

## Tasks

### Task 1: Create a Linux virtual machine and install Nginx
From Cloud Shell, run the following az vm create command to create a Linux VM:
   az vm create --resource-group "learn-05639575-fb29-41b6-8275-21ec42dcfbf5" --name my-vm --public-ip-sku Standard --image Ubuntu2204 --admin-    username azureuser --generate-ssh-keys

  
Run the following az vm extension set command to configure Nginx on your VM:
   az vm extension set --resource-group "learn-05639575-fb29-41b6-8275-21ec42dcfbf5" --vm-name my-vm --name customScript --publisher Microsoft.Azure.Extensions --version 2.1 --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'
