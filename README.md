# Ansible role for MySQL 5.7
Ansible role for MySQL 5.7 installation for CentOS 7

## What's inside?
1. Interesting MySQL dirs and files: 
    ```
    /var/log/mysqld.log
    /etc/yum.repos.d/mysql-community.repo
    ```
2. Custom settings as per `defaults/main.yml`
3. Temporary root password is located in `/var/log/mysqld.log `
    ```
    sudo grep 'temporary password' /var/log/mysqld.log
    ```
4. Updated root password: `root`

## Tested on
mysql  Ver 14.14 Distrib 5.7.25, for Linux (x86_64) using  EditLine wrapper

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
- InnoDB Startup Options and System Variables [https://dev.mysql.com/doc/refman/5.7/en/innodb-parameters.html]()
- Server Command Options [https://dev.mysql.com/doc/refman/5.7/en/server-options.html]()
- Query Cache Configuration [https://dev.mysql.com/doc/refman/5.7/en/query-cache-configuration.html]()
- mysql_db – Add or remove MySQL databases from a remote host [https://docs.ansible.com/ansible/latest/modules/mysql_db_module.html]()
- Improving Magento Performance With MySQL Query Cache [https://www.crucialhosting.com/knowledgebase/improving-magento-performance-mysql-query-cache]()
- Magento + MySQL Query Cache: A Case Study [https://maxchadwick.xyz/blog/magento-mysql-query-cache-case-study]()

## TO DO
-[ ] add dependencies
-[ ] investigate my.cnf options for best Magento 2 performance (eg. mysql_innodb_flush_log_at_trx_commit, query cache)
-[ ] check tunig tool [https://raw.githubusercontent.com/major/MySQLTuner-perl/master/mysqltuner.pl]()
 
## License
Copyright (c) We Are Interactive under the MIT license.