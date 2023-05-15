bootstrap
=========

Ansible role that bootstraps a new server with all the required packages and configurations

Tags
------------

- update # this tag will run the task necessary for updating the server
- dotfiles # this tag will run the task to update the dotfiles

Role Variables
--------------

```yaml
users:
  - username: root
timezone: US/Pacific
ssh_port: 22
```

Dependencies
------------

```yaml
roles:
  - gantsign.oh-my-zsh
```

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    role: darsh12.bootstrap
    vars:
    users:
      - username: root
      - username: user
    timezone: US/Pacific
    ssh_port: 22

```

License
-------

BSD

Author Information
------------------

darsh12
