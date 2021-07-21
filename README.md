MySQL
=========

A simple Ansible role for installing and configuring the MySQL 8 RHEL/CentOS 8 and Rocky Linux using AWX or Tower.

Install the necessary packages;
Create User;
Create Database.


Requirements
------------

- The SELinux and firewall settings are not considered to be a concern of this role.

Role Variables
--------------


Variables below are required

| Variable                                     | Default                       | Comments
| :---                                         | :---                          | :---
|                                              |                               |
| `mysql_AWX_TOWER_root_user`                  | root                          |
|                                              |                               |
| `mysql_AWX_TOWER_root_pass`                  |                               | Inform root password
|                                              |                               |
| `mysql_AWX_TOWER_new_db`                     |                               | Inform new database name
|                                              |                               |
| `mysql_AWX_TOWER_db_user`                    |                               | Inform DB user name
|                                              |                               |
| `mysql_AWX_TOWER_db_user_pass`               |                               | Inform DB user password
|                                              |                               |
| `mysql_AWX_TOWER_db_user_src`                |                               | Inform DB user src IP address
|                                              |                               |

Dependencies []
------------

Attention
---------
When you run a second time on the same server to just create a new database and a new user, it must be used in the following way below.

```yml
ansible-playbook you_playbook.yml --skip-tags "root_pass"
```

## Contributing
Issues, feature requests, ideas are appreciated and can be posted in the Issues section.


Author Information
------------------
LinkedIn: https://br.linkedin.com/in/almircandido
