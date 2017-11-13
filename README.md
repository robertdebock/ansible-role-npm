NPM
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

- robertdebock.epel

Example Playbook
----------------

```
---
- hosts: servers
  become: yes

  roles:
     - npm

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
