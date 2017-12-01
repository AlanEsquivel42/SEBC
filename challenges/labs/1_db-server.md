MariaDB [(none)]> select @@hostname;
+------------------------------+
| @@hostname                   |
+------------------------------+
| ip-172-31-5-226.ec2.internal |
+------------------------------+
1 row in set (0.00 sec)

MariaDB [(none)]> select @@version;
+----------------+
| @@version      |
+----------------+
| 5.5.56-MariaDB |
+----------------+
1 row in set (0.00 sec)

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
+--------------------+
8 rows in set (0.00 sec)