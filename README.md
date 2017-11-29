npm
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-npm.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-npm)

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

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Example Playbook
----------------

```
---
- hosts: servers
  become: yes

  roles:
     - robertdebock.npm

  tasks:
    - name: install package with npm
      npm:
        name: debug
        global: yes
```

Install this role using `galaxy install robertdebock.npm`.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>
