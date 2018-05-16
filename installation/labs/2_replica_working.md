## <center> <a name="MYSQL replication"/> Installation Lab: MYSQL Replica
* Installed mariaDB in 2 hosts.
* Installed mysql java connector in all the participating hosts.
* Updated thc onfiguration file /etc/my.cnf. set the service-id to 2 & 3 respectively for master and slave.
* Started the mysqld service
* On the master MySQL node, granted replication privileges for your replica node:
	* Log in with mysql -u ... -p 
	* mysql> GRANT REPLICATION SLAVE ON *.* TO 'slaveuser'@'%' IDENTIFIED BY 'Cloudera';
	* mysql> SET GLOBAL binlog_format = 'ROW'; 
	* mysql> FLUSH TABLES WITH READ LOCK;
* Run this from slave to get the db and tables -> mysqldump -h 172.31.5.153 -u root -p --databases scm > scm.sql
* Run this from slavemysqldump -u root -p scm > scm.sql
* In a second terminal session, log into the MySQL master and show its status:
	* mysql> SHOW MASTER STATUS;
	* Make note of the file name and byte offset. The replica needs this info to sync to the master.
	* Logout of the second session; remove the lock on the first with mysql> UNLOCK TABLES;
* Login to the replica server and configure a connection to the master:
	* mysql> CHANGE MASTER TO MASTER_HOST='ec2-18-220-61-58.us-east-2.compute.amazonaws.com', MASTER_USER='slaveuser', MASTER_PASSWORD='Cloudera', MASTER_LOG_FILE='mysql_binary_log.000007', MASTER_LOG_POS=1550;;
* Initiate slave operations on the replica
	* mysql> START SLAVE;
	* mysql> SHOW SLAVE STATUS \G