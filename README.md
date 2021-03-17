# passwordless_login
configuring passwordless authentication from control node to 100 target servers

## Purpose

This Ansible Playbook will assist on establishing passwordless SSH logins with the remote hosts you wish to manage. Passwordless logins is a great convenience when connecting to multiple servers, via Ansible or not!

---

## Download the tool

Clone the repository to your ansible-enabled host:

```bash
git clone https://github.com/nitinanjankar/passwordless_login.git
```

---

## Prerequisites

Make sure your Ansible host is equipped with the utilities, and that they are available to the PATH of the user you will be running the playbook as.

- ssh-keygen
- ssh-copy-id
- sshpass

If you dont have them, before continuing you will have to install them using the recommended ways for your Linux distribution.

---

## Preparations before you run

Edit the `hosts` file and define your environment's information. Fill in using the below matrix:

| Name | Description |
| ----------------------- | ---------------------------------------------- |
| ansible_user | User of your localhost AND remote machines. If you are applying the procedure to multiple hosts, It must be common. |
| ansible_password | The password of your localhost's and remote_machine_username account |
| ansible_svc | User service account to create passwordless authentication |
| control_node | If you want to define the IP of your local_host |
| [target_nodes] | Fill in the list of hosts that you want to establish the passwordless login with. |

If you are planning to run the script towards multiple hosts, make sure the username/password you defined is the same to all of them!

---

## How to run it

run:

```
cd passwordless_login

export ANSIBLE_HOST_KEY_CHECKING=False

ansible-playbook passwordless_authentication.yml 

```
