```
[root@clouderaseb00 ~]# service mysqld status
mysqld (pid  2861) is running...
[root@clouderaseb00 ~]# hostname
clouderaseb00.gitcluster.com
[root@clouderaseb00 ~]# mysql --version
mysql  Ver 14.14 Distrib 5.5.53, for Linux (x86_64) using readline 5.1
[root@clouderaseb00 ~]# mysql -u root -p
Enter password:
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 5.5.53-log MySQL Community Server (GPL)

Copyright (c) 2000, 2016, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hue                |
| metastore          |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.01 sec)

mysql>

```

