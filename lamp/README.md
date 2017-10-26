run 2 docker containers 
docker run -i -t  centos:ansiclient /bin/bash
docker run -i -t  centos:ansiclient /bin/bash
name 172.17.0.2 (webserver)
     172.17.0.3 (dbserver)
respectively

now clone the LAMP play book from git 

git clone git@github.com:Lforlinux/ansible.git

edit host file and place our docker ip over there

#ansible-playbook -i hosts site.yml --check
#ansible-playbook -i hosts site.yml 


