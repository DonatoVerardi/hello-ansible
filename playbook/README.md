# hello-ansible

This is my lab space to learn ansible.

https://www.javatpoint.com/ansible


## Playbook

Get IP Address of the docker container in the inventory:

$ SSH_IPADDRESS=$(docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' openssh-server)
$ echo $SSH_IPADDRESS "  ansible_connection=ssh ansible_ssh_user=donato ansible_ssh_pass=password ansible_ssh_port=2222" > inventory

Check Playbook

$ ansible-playbook -i inventory playbook.yml --check

Play Playbook

