# hello-ansible

This is my lab space to learn ansible.

First, run a docker container on which you can ssh and install stuff.

$ docker-compose -f ./docker/docker-compose.yaml up -d

Get IP Address:

$ SSH_IP=$(docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' openssh-server)

SSH to this IP Address 

$ ssh donato@$SSH_IP -p 2222

Enter "password"
donato@172.19.0.2's password: 
Welcome to OpenSSH Server

Install python:

$ sudo su

$ apk add --update --no-cache python3 && ln -sf python3 /usr/bin/python && python3 -m ensurepip && pip3 install --no-cache --upgrade pip setuptools 

