# Programing-Assessment-Bosch
Create deployment scripts using Ansible to deploy an application to some target servers (or virtual machines)

Infra Setup
-----------------
Ansible Master - 3.109.144.189
Deploymnent App -  IP (where the todo application deployed)
application url: http://13.233.200.70:3000

Ansible Setup:
----------------
1.  Ansible has two roles and one playbook
    a. Docker - This role is used to install docker & docker-compose on the target node
    b. getting-started - This role is used to build the docker image and deploy the app on target node with docker-compose
    c. getting-started-plybook.yml - This is the playbook to execute the roles
    d. inventory-file - This is the inventory files need to pass while running the playbook

2. ansible execution command
    ansible-playbook -i inventory-file getting-started-playbook.yml

3. after successful execution of playbook we can access the todo app on fallowing url: http://13.233.200.70:3000
