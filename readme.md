# Ansible roles

A set of ansible roles for CI/CD environment :

 - **Common role**: for shared libraries
 - **Jenkins role**: to run Jenkins on a container
 - **Nexus role** : to run Nexus on a container
 - **Sonar role** : to run Sonar on a container.
 - **Postgres role**: a db used by sonar to store tests results.

## Pre-requisites :

 - ansible user on each node.
 - ssh established with sudo permission to ansbile user.
 - *I don't remember right now.*

## How to run

First make sure to customize all the variables in each role `vars/main.yml` file.

```bash
  $   ansible-playbook index.yml
```

## Notes:

This project can work also on multi-hosts containers, meaning that, you can run each container on a different host, you just need to configure the variables for each role to point to your hostname/ip container's host with the corresponding mapped port in each role in `vars/main.yml`.
