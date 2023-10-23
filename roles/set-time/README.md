Settime
=========

Set timezone by time_zone variable

Requirements
------------

none

Role Variables
--------------

time_zone='Asia/Taipei'

Dependencies
------------

none

Example Playbook
----------------

## Notice 

There is two ways to impletement this feature:

1. declare variable in default/vars yml.
2. declare host with time_zone in host file.

host example
```
[all:vars]
...

[dev-hosts]
10.1.169.159 time_zone='Asia/Taipei'
10.1.169.160 time_zone='Asia/Tokyo'


```

ansible-playbook -i host setup.yml

License
-------

BSD

Author Information
------------------

scott.yen@light-morning.com
