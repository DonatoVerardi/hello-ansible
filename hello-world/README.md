# hello-ansible

This is my lab space to learn ansible.

https://www.ansibletutorials.com/


## Hello World


With full names of the parameters

$ ansible all --inventory "localhost," --module-name debug --args "msg='Hello Ansible'"

With short names of the parameter

$ ansible all -i "localhost," -m debug -a "msg='Hello Ansible'"

Using a inventory file

$ ansible all -i ./inventory -m debug -a "msg='Hello Ansible'"

