bootstrap
=========

Ansible role that bootstraps a new server with all the required packages and configurations. Additionally, you can optionally add a new user

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
new_username: user (optional)
user_password: password (optional, prompted if left blank and when new_username is defined)
ssh_public_keys: ['ssh-key'] (optional)
user_uid: <DEFAULT BLANK>
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
    new_username: user
    user_password: password
    ssh_public_keys: ['ssh-key']

```

License
-------

BSD

Author Information
------------------

darsh12
