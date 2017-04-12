# interkonect.com

Ansible provisioning and deployment for my websites.

## Installation

Create new cloud server using Ubuntu 16.04 LTS (64 bit) as the base image and adding
your public SSH key. The hostname should be `interkonect.com`.

### Install Ansible locally

```
apt-add-repository ppa:ansible/ansible
apt-get update
apt-get install ansible
```

## Provision Servers

```
ansible-playbook provision/interkonect.com/main.yml
```

## Deploy websites

```
ansible-playbook deploy/interkonect.com/main.yml
```

## Misc

Show facts for servers:

```
ansible all -m setup
```


