mysql_grants
============

[![Build Status](https://travis-ci.org/andrelohmann/ansible-role-mysql_grants.svg?branch=master)](https://travis-ci.org/andrelohmann/ansible-role-mysql_grants)

Use this role to provision mysql grants

Requirements
------------

This role requires debian or ubuntu and an installed mysql database

Role Variables
--------------

The default set of variables can be used to provisions users and grants

    mysql_grants_databases:
    - name: mytest
      encoding: utf8
    mysql_grants_users:
    - name: tesuser
      password: testpassword
      host: localhost
      priv: 'mytest.*:ALL'
      state: present



Example Playbook
----------------

    - hosts: mysql
      become: yes
      roles:
         - andrelohmann.mysql_grants

License
-------

MIT

Author Information
------------------

https://github.com/andrelohmann
