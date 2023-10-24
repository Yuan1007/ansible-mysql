Role Name
=========

Add / Update / Delete user account (password / ssh keys)

Requirements
------------

add_users setting in vars/main.yml
delete_users setting in vars/main.yml (optional)

Role Variables
--------------

add_users
delete_users

example
```
add_users:
  - { name: yuan, sudoer: true }
delete_users:
  - { name: test }

```

Dependencies
------------

sethostname
settime

Example Playbook
----------------

ansible-playbook -i host setup.yml 

License
-------

BSD

Author Information
------------------

