ansible-role-froxlor
=========

Simple ansible-role to install [froxlor](https://froxlor.org).

Requirements
------------
This role was created for Debian 10.x (Buster). It is configured to work with [froxlor](https://froxlor.org). You might use this role in conjunction with the roles:

* ansible-role-apache
* ansible-role-mysql
* ansible-role-dovecot
* ansible-role-postfix

Role Variables
--------------
In `defaults/main.yaml` the following variables and default-values are specified.

```yaml
http_user: www-data
http_group: www-data

froxlor_admin_user: admin
activate_froxlor_newsfeed: true
```

The following variables don't have defaults. You need to specify them either in a file in group_vars, host_vars directory or via command-line.

```yaml
froxlor_mysql_password: Password for the froxlor mysql database
mysql_admin_password: Password of the mysql administrator
server_fqdn: Fully quallified domain name of the froxlor-server
server_ip: IP of the froxlor-server.
froxlor_admin_password: Administrator password for froxlor

```

Example Playbook
----------------
This role can be easily used in a playbook like this: 

```yaml
- hosts: froxlor-servers
  roles:
      - ansible-role-froxlor
```

License
-------
GNU GENERAL PUBLIC LICENSE VERSION 3

Author Information
------------------
[blog.retter.jetzt](https://blog.retter.jetzt)
