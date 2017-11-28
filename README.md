ansible-role-npm
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

- robertdebock.ansible-role-epel

Download the dependencies by issueing this command:
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
     - robertdebock.ansible-role-npm

  tasks:
    - name: install package with npm
      npm:
        name: debug
        global: yes
```

Install this role using `galaxy install robertdebock.ansible-role-npm`.

License
-------

Apache License, Version 2.0

Author Information
------------------

Robert de Bock <robert@meinit.nl>
