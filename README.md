Role Name
=========

Have NPM available.

Requirements
------------

On RHEL (platform: EL) the epel repository is required.

Role Variables
--------------

None known.

Dependencies
------------

- robertdebock.epel

Example Playbook
----------------

```
---
- hosts: servers
  become: yes
  roles:
     - npm
```

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>
