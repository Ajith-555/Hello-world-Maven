#Java Web Application

This POC has been done with complete CI/CD process. Code will be pushed to GitHub (SCM). Jenkins will pull the code and run the job based on poll SCM and build the code ( *.war file ).

Jenkins Server : Post build setup has been configured  ( Execute command over SSH ).It does execute the commands on Ansible Master Remote server. It takes the Docker file and build the image and versioning and push it to Docker hub and delete the image on Ansible Master server.

Ansible Master Server : A simple ansible playbook has been written on Ansible master server. Playbook will also be executed on publish over SSH. Host has been added with master Ansible with password authentication on, so that connection can be established between the Ansible host.

Ansible host Server : Ansible host will pull the images from docker hub and run the image on port 8090.
