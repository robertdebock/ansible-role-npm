npm
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-npm.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-npm)

Have NPM available on your system.

[Unit tests](https://travis-ci.org/robertdebock/ansible-role-npm) are done on every commit and periodically.

If you find issues, please register them in [GitHub](https://github.com/robertdebock/ansible-role-npm/issues)

To test this role locally please use [Molecule](https://github.com/metacloud/molecule):
```
pip install molecule
molecule test
```
There are many scenarios available, please have a look in the `molecule/` directory.

Context
--------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/drawings/artifacts/npm.png "Dependency")

Requirements
------------

Access to a repository containing packages, likely on the internet.
On RHEL (platform: EL) the EPEL repository is required.

Role Variables
--------------

None known.

Dependencies
------------

You can prepare your system using these roles:

- [robertdebock.bootstrap](https://travis-ci.org/robertdebock/ansible-role-bootstrap)
- [robertdebock.epel](https://travis-ci.org/robertdebock/ansible-role-epel)

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.4|ansible 2.5|ansible 2.6|
|------------|-----------|-----------|-----------|
|alpine-edge|yes|yes|yes|
|alpine-latest|yes|yes|yes|
|archlinux|yes|yes|yes|
|centos-6|no|no|no|
|centos-latest|yes|yes|yes|
|debian-buster|no|no|no|
|debian-stretch|no|no|no|
|fedora-latest|yes|yes|yes|
|fedora-rawhide|no|no|no|
|opensuse-leap|yes|yes|yes|
|opensuse-tumbleweed|no|no|no|
|ubuntu-artful|yes|yes|yes|
|ubuntu-latest|yes|yes|yes|

Example Playbook
----------------

```
---
- hosts: servers
  become: yes

  roles:
     - role: robertdebock.bootstrap
     - role: robertdebock.epel
     - role: robertdebock.npm

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

[Robert de Bock](https://robertdebock.nl/) <robert@meinit.nl>
