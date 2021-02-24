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

Alternatively, you can download the `ansible_setup_passwordless_ssh.yml` and `hosts` from this repository.

---

## Prerequisites

Make sure your Ansible host is equipped with the utilities, and that they are available to the PATH of the user you will be running the playbook as.

- ssh-keygen
- ssh-copy-id
- sshpass

If you dont have them, before continuing you will have to install them using the recommended ways for your Linux distribution.

---

## How to run it

run:

```
cd passwordless_login

ansible-playbook passwordless_authentication.yml 

```
