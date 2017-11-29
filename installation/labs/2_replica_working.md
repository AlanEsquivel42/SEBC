**Maria dB**

yum install -y mariadb-server  
systemctl stop mariadb  
vi /etc/my.cnf  
  
[mysqld]  
transaction-isolation = READ-COMMITTED  
# Disabling symbolic-links is recommended to prevent assorted security risks;  
# to do so, uncomment this line:  
# symbolic-links = 0  
  
key_buffer = 16M  
key_buffer_size = 32M  
max_allowed_packet = 32M  
thread_stack = 256K  
thread_cache_size = 64  
query_cache_limit = 8M  
query_cache_size = 64M  
query_cache_type = 1  
  
max_connections = 550  
#expire_logs_days = 10  
#max_binlog_size = 100M  
  
#log_bin should be on a disk with enough free space. Replace '/var/lib/mysql/mysql_binary_log' with an appropriate path for your system  
#and chown the specified folder to the mysql user.  
log_bin=/var/lib/mysql/mysql_binary_log  
  
binlog_format = mixed  
  
read_buffer_size = 2M  
read_rnd_buffer_size = 16M  
sort_buffer_size = 8M  
join_buffer_size = 8M  
  
# InnoDB settings  
innodb_file_per_table = 1  
innodb_flush_log_at_trx_commit  = 2  
innodb_log_buffer_size = 64M  
innodb_buffer_pool_size = 4G  
innodb_thread_concurrency = 8  
innodb_flush_method = O_DIRECT  
innodb_log_file_size = 512M  
  
[mysqld_safe]  
log-error=/var/log/mariadb/mariadb.log  
pid-file=/var/run/mariadb/mariadb.pid  
  
systemctl enable mariadb  
systemctl start mariadb  
  
$ sudo /usr/bin/mysql_secure_installation  
[...]  
Enter current password for root (enter for none):  
OK, successfully used password, moving on...  
[...]  
Set root password? [Y/n] y  
New password:  
Re-enter new password:  
[...]  
Remove anonymous users? [Y/n] y  
[...]  
Disallow root login remotely? [Y/n] n  
[...]  
Remove test database and access to it [Y/n] y  
[...]  
Reload privilege tables now? [Y/n] y  
 ... Success!  
  
wget https://dev.mysql.com/downloads/file/?id=472650  
tar zxvf mysql-connector-java-5.1.44.tar.gz  
mkdir -p /usr/share/java/cp mysql-connector-java-5.1.44/mysql-connector-java-5.1.44-bin.jar /usr/share/java/mysql-connector-java.jar  
  
$ mysql -u root -p  
MariaDB [(none)]> create database amon DEFAULT CHARACTER SET utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]> grant all on amon.* TO 'amon'@'%' IDENTIFIED BY 'amon';  
Query OK, 0 rows affected (0.00 sec)  
  
MariaDB [(none)]> create database rman DEFAULT CHARACTER SET utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]> grant all on rman.* TO 'rman'@'%' IDENTIFIED BY 'rman';  
Query OK, 0 rows affected (0.00 sec)  
  
MariaDB [(none)]> create database metastore DEFAULT CHARACTER SET utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]> grant all on metastore.* TO 'hive'@'%' IDENTIFIED BY 'hive';  
Query OK, 0 rows affected (0.00 sec)  
  
MariaDB [(none)]> create database sentry DEFAULT CHARACTER SET utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]> grant all on sentry.* TO 'sentry'@'%' IDENTIFIED BY 'sentry';  
Query OK, 0 rows affected (0.00 sec)  
  
MariaDB [(none)]> create database nav DEFAULT CHARACTER SET utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]> grant all on nav.* TO 'nav'@'%' IDENTIFIED BY 'nav';  
Query OK, 0 rows affected (0.00 sec)  
  
MariaDB [(none)]> create database navms DEFAULT CHARACTER SET utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]> grant all on navms.* TO 'navms'@'%' IDENTIFIED BY 'navms';  
Query OK, 0 rows affected (0.00 sec) 
  
MariaDB [(none)]> create database scm DEFAULT CHARACTER SET utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]> grant all on scm.* TO 'scm'@'%' IDENTIFIED BY 'scm';  
Query OK, 0 rows affected (0.00 sec)   
  
MariaDB [(none)]> create database hue DEFAULT CHARACTER SET utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]> grant all on hue.* TO 'hue'@'%' IDENTIFIED BY 'hue';  
Query OK, 0 rows affected (0.00 sec) 
  
MariaDB [(none)]> create database oozie default character set utf8;  
Query OK, 1 row affected (0.00 sec)  
  
MariaDB [(none)]>  grant all privileges on oozie.* to 'oozie'@'localhost' identified by 'oozie';  
Query OK, 0 rows affected (0.00 sec)  
  
MariaDB [(none)]>  grant all privileges on oozie.* to 'oozie'@'%' identified by 'oozie';  
Query OK, 0 rows affected (0.00 sec)  
  

