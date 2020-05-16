---
layout: post
title:  "Fix MySql User Permission Issue in Ubuntu 16.04"
date:   2016-08-15 21:03:36 +0530
categories: Shell Vim
---
Problem: [http://stackoverflow.com/questions/38098505/mysql-works-with-sudo-but-without-not-ubuntu-16-04-mysql-5-7-12-0ubuntu1-1/38098680](http://stackoverflow.com/questions/38098505/mysql-works-with-sudo-but-without-not-ubuntu-16-04-mysql-5-7-12-0ubuntu1-1/38098680)

Solution: [http://askubuntu.com/questions/766334/cant-login-as-mysql-user-root-from-normal-user-account-in-ubuntu-16-04](http://askubuntu.com/questions/766334/cant-login-as-mysql-user-root-from-normal-user-account-in-ubuntu-16-04)


Step By Step Process -

#### Ordered
1. First, connect in sudo mysql
```
sudo mysql -u root
```
2. Check your accounts present in your db
```
SELECT User,Host FROM mysql.user;
+------------------+-----------+
| User             | Host      |
+------------------+-----------+
| admin            | localhost |
| debian-sys-maint | localhost |
| magento_user     | localhost |
| mysql.sys        | localhost |
| root             | localhost |
```
3. Delete current root@locslhost account
```
mysql> DROP USER 'root'@'localhost';
Query OK, 0 rows affected (0,00 sec)
```
4. Recreate your user
```
mysql> CREATE USER 'root'@'%' IDENTIFIED BY '';
Query OK, 0 rows affected (0,00 sec)
```
5. Give permissions to your user (don't forget to flush privileges)
```
mysql> GRANT ALL PRIVILEGES ON *.* TO 'root'@'%';
Query OK, 0 rows affected (0,00 sec)

mysql> FLUSH PRIVILEGES;
Query OK, 0 rows affected (0,01 sec)
```
6. Exit mysql and try to reconnect without sudo
