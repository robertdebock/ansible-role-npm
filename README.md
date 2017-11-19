ansible-role-npm
=========

Have NPM available on your system.

Requirements
------------

Access to a repository containing packages, likely on the internet.
On RHEL (platform: EL) the epel repository is required.

Role Variables
--------------

None known.

Dependencies
------------

- robertdebock.ansible-role-epel

Example Playbook
----------------

```
---
- hosts: servers
  become: yes

  roles:
     - ansible-role-npm

  tasks:
    - name: install package with npm
      npm:
        name: debug
        global: yes
```

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>
