ansible-role-hostnames
=========

Hostname configuration for EL systems.

Requirements
------------

This role has only been tested on EL 6 systems. EL 7 system support is anticipated in the future.

Role Variables
--------------

__role\_hostnames\_hostname\_short__: Short hostname value (i.e. web01). This setting defaults to the builtin Ansible environment variable named inventory_hostname_short.

__role\_hostnames\_etc\_hosts\_lines__: A list of complete lines to be included in /etc/hosts. Defaults to an empty list and will be skipped.

Example:
```
[
'192.168.10.1  web01.demoapp.com  web01',
'192.168.10.2  web02.demoapp.com  web02'
]
```

Example Playbook
----------------

Override the above variables by modifying your project's group_vars or host_vars.

```
- hosts: servers
  roles:
    - { role: bitmotive.ansible-role-hostnames, tags: "hostnames,common" }
```

License
-------

MIT
