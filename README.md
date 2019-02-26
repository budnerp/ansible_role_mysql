# Ansible role for MySQL 5.7
Ansible role for MySQL 5.7 installation for CentOS 7

## What's inside?
1. Interesting MySQL dirs and files: 
    ```
    /var/log/mysqld.log
    /etc/yum.repos.d/mysql-community.repo
    ```
2. Custom settings as per defaults/main.yml
3. Temporary root password is located in /var/log/mysqld.log 
    ```
    sudo grep 'temporary password' /var/log/mysqld.log
    ```
4. Updated root password: root   
## Tested on

## Installation
1. Navigate to Ansible's roles folder
2. Add the repo to git modules
    ```
    git submodule add https://github.com/budnerp/ansible_role_mysql.git ansible_role_mysql
    ```
3. Add the role to Ansible's playbook file
    ```    
    roles:
    [...]
        - ansible_role_mysql
    [...]
    ```

## Other links
- MySQL Yum Repository [https://dev.mysql.com/downloads/repo/yum/]()
- A Quick Guide to Using the MySQL Yum Repository [https://dev.mysql.com/doc/mysql-yum-repo-quick-guide/en/]()
- Server Command Options [https://dev.mysql.com/doc/refman/5.7/en/server-options.html]()
- mysql_db – Add or remove MySQL databases from a remote host [https://docs.ansible.com/ansible/latest/modules/mysql_db_module.html]()

## TO DO
-[ ] add dependencies

## License
Copyright (c) We Are Interactive under the MIT license.