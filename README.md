npm
=========

[![Build Status](https://travis-ci.org/robertdebock/ansible-role-npm.svg?branch=master)](https://travis-ci.org/robertdebock/ansible-role-npm)

Have NPM available on your system.

Context
--------
This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/robertdebock.github.io/artifacts/npm.png "Dependency")

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

- robertdebock.bootstrap
- robertdebock.epel

Download the dependencies by issuing this command:
```
ansible-galaxy install --role-file requirements.yml
```

Compatibility
-------------

This role has been tested against the following distributions and Ansible version:

|distribution|ansible 2.3|ansible 2.4|ansible 2.5|
|------------|-----------|-----------|-----------|
|alpine-3.6|yes|yes|yes|
|alpine-3.7|yes|yes|yes|
|archlinux|yes|yes|yes|
|centos-7|yes|yes|yes|
|debian-jessie|yes|yes|yes|
|fedora-26|yes|yes|yes|
|fedora-27|yes|yes|yes|
|opensuse-42.2|yes|yes|yes|
|opensuse-42.3|yes|yes|yes|
|ubuntu-artful|yes|yes|yes|
|ubuntu-xenial|yes|yes|yes|

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

Robert de Bock <robert@meinit.nl>
