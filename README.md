# tikal01

This repo contains the code for installing Docker on target machine and bring up a container on it. 

#hosts file

Contains the target machines IP(s), the private key file path and the user name on target machine. 
User on target machine should be sudoer. 
User on target machine should be configured for no asking password. PLS configure that in /etc/sudoers. Add the following line:
<user name> ALL=(ALL) NOPASSWD:ALL
  
#install docker 
ansible-playbook docker.yml -i ./hosts 

#deploy container
ansible-playbook deploy.yml -i ./hosts 

