# Exercise 2: Configure network access

## Task

### Task 1: Access your web server
- Run the following az vm list-ip-addresses command to get your VM's IP address and store the result as a Bash variable:


- Run the following curl command to download the home page:


- As an optional step, try to access the web server from a browser:


- Run the following to print your VM's IP address to the console:


- Copy the IP address that you see to the clipboard.
- Open a new browser tab and go to your web server. After a few moments, you see that the connection isn't happening. If you wait for the browser to time out, you see something like this:


- Keep this browser tab open for later.


### Task 2: List the current network security group rules
- Run the following az network nsg list command to list the network security groups that are associated with your VM:


- Run the following az network nsg rule list command to list the rules associated with the NSG named my-vmNSG:


- Run the az network nsg rule list command a second time. This time, use the --query argument to retrieve only the name, priority, affected ports, and access (Allow or Deny) for each rule. The --output argument formats the output as a table so that it's easy to read:

### Task 3: Create the network security rule
- Run the following az network nsg rule create command to create a rule called allow-http that allows inbound access on port 80:

  
- To verify the configuration, run az network nsg rule list to see the updated list of rules:


### Task 4: Access your web server again
-  Run the same curl command that you ran earlier:


- As an optional step, refresh your browser tab that points to your web server. You see the home page:

  
