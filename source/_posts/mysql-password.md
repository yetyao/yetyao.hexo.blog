---
title: mysql8.0.12忘记密码
date: 2020-07-15 20:18:59
tags: mysql
categories: mysql
---


1. 修改 /etc/my.cnf
2. 添加 skip-grant-tables
3. systemctl restart mysqld
4. mysql -u root -p (root身份登录)
5. use mysql
6. flush privileges
7. alter user ‘root‘@’localhost’ IDENTIFIED BY ‘mypassword’;