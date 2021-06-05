# ELK-Project

The main purpose of this network is to configure an ELK stack server and monitor the system.  The newtork included a  load balanced.  Load balancing ensures that the application will be highly accessible, in addition to restricting access to the network. 
A jump box was used to restrict the IP addresses that communicate to the jump box and it helps to prevent the Azure virtual machines from being exposed to the public. 

## ELK Stack Diagram
 ![](https://github.com/S-Varel/ELK-Project/blob/main/ELK%20Project%20Diagram.png)


### Process used in ELK Project
Note:The files in this repository were used to configure the network.


Created a VNET to allow the virtual machines to securely communicate with each other and the Internet. 
Created a Resource Group (RedTeam). This allows for the grouping of resources to enusre the creation and de-provisioning are unified. 
Created a Peer connection between the vNets to allow traffic to pass through the Vnets and regions bi-directionally.

Created a new VM (ELK Server)-connected the ELK server to the ansible container using the public key. 

Created ELK Ansible playbook to install 
* docker.io
* python3-pip
* docker

See ELK ansible playbook [here](https://github.com/S-Varel/ELK-Project/blob/main/ELK.yml)

Created an Ansible Host yml file to identify the IP addresses used to connect the webservers and the ELK server

See Ansible Host.yml [here](https://github.com/S-Varel/ELK-Project/blob/main/Host.yml)

Created rules for the ELK-VM-NSG (network security group)
	Since the ELK server runs on port 5601 created a rule to allow the TCP traffic from my IP address over port 5601.  

Installed Filebeat on the DVWA Container
The filebeat book installs the Linux Filebeat instructions to download and install the .deb file. The playbook will enable, setup and start the filebeat modules. 

See Filebeat-Playbook [here](https://github.com/S-Varel/ELK-Project/blob/main/Filebeat-Playbook.yml)

Once the filebeat installation was successfully run the ELK Stack successfully received logs.
