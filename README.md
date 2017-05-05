# interkonect.com

Ansible provisioning and deployment for my websites with SSL certficates from
[Lets Encrypt](https://letsencrypt.org).

## Installation

Ansible is installed on a control node, typically a developers machine. This
repository contains the hosts and playbooks for provisioning and deployment.

### Install Ansible

Ansible 2.x or better is required.

#### Ubuntu

```
apt-add-repository ppa:ansible/ansible
apt-get update
apt-get install ansible
```

### Clone Repository

```
git clone git@github.com:krisleech/interkonect-server.git
cd interkonect-server
```

## Provision Servers

Create new cloud server using Ubuntu 16.04 LTS (64 bit) as the base image and adding
your public SSH key. The hostname should be `interkonect.com`. There is assumed
to be a root user.

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
