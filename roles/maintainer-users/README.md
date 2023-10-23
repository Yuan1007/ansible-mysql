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
  - { name: root, password: $2y$10$7P9Gx1vpOzBQ8Q4JLCu.he1lNMwp64rwY.pVMHOY1swPSzXD3.SXC, sudoer: true }
  - { name: ubuntu, password: $2y$10$7P9Gx1vpOzBQ8Q4JLCu.he1lNMwp64rwY.pVMHOY1swPSzXD3.SXC, sudoer: true } # 26597795
  - { name: scott, sudoer: true, groups: ['docker'] }
  - { name: areal, sudoer: true }
  - { name: gimmy, password: $2y$10$9/QHbyoK1htbvjBuVmUQ4OgvSaF3zXDNqr6Ljq..gC1AG69f9rFnK, sudoer: true } # gimmy5566978
  - { name: ching, sudoer: true }
  - { name: cheng, sudoer: true }
  - { name: jinga, sudoer: true }
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

scott.yen@light-morning.com
