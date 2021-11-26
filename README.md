ansible_role_sshkey
=========


[![CI](https://github.com/habbis/ansible_role_sshkey/workflows/CI/badge.svg)](https://github.com/habbis/ansible_role_sshkey/actions?query=workflow%3ACI)


This role manage sshkeys for users and by default only root is added see
the task


Example site.yml

```
---
- name: setup puppet agent
  gather_facts: yes
  remote_user: root
  #remote_user: ansible
  #become: yes
  #become_method: sudo
  hosts: test
  #hosts: puppet-clients
  #hosts: all
  vars_files:
    -  defaults/main.yml
    #-  defaults/secrets.yml

  roles:
    - { role: ../ansible_role_sshkey }
```
