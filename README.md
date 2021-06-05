# ELK-Project

The main purpose of this network is to configure an ELK stack server and monitor the system.  The newtork included a  load balanced and monitored instance of DVWA.  Load balancing ensures that the application will be highly accessible, in addition to restricting access to the network. 
A jump box was used to restrict this to e IP addresses that communicate to the jomp box and it helps to prevent the azure virtual machines from being exposed to the public. 

## ELK Stack Diagram

![] (Elk Project Diagram.png)



The files in this repository were used to configure the network.


Created a VNET to allow the virtual machines to securely communicate with each other and the internet. 
Created a Resource Group (RedTeam). This allows for the grouping of resources to enusre the creation and de-provisioning are unified. 
Created a Peer connection between the vNets to allow traffic to pass through the Vnets and regions in bi-directionally.

Created a new VM (ELK Server)-connected the ELK server to the ansible container using the public key. 

Created ELK Ansible playbook to install 
	*docker.io
	*python3-pip
	*docker

