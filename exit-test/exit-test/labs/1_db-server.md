## <center> DB setup

* The command hostname -f and its output

[root@ip-172-31-25-114 ec2-user]# hostname -f
ip-172-31-25-114.us-east-2.compute.internal

* The command mysql -u <user> -p<password> -e "status;" and its output

[root@ip-172-31-25-114 ec2-user]# mysql -u root -p -e "status;"
Enter password:
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          13
Current database:
Current user:           root@localhost
SSL:                    Not in use
Current pager:          stdout
Using outfile:          ''
Using delimiter:        ;
Server:                 MariaDB
Server version:         5.5.56-MariaDB MariaDB Server
Protocol version:       10
Connection:             Localhost via UNIX socket
Server characterset:    latin1
Db     characterset:    latin1
Client characterset:    utf8
Conn.  characterset:    utf8
UNIX socket:            /var/lib/mysql/mysql.sock
Uptime:                 12 min 55 sec

Threads: 1  Questions: 49  Slow queries: 0  Opens: 1  Flush tables: 2  Open tables: 27  Queries per second avg: 0.063
--------------


* The command mysql -u <user> -p<password> -e "show databases;" and its output


[root@ip-172-31-25-114 ec2-user]# mysql -u root -p -e "show databases;"
Enter password:
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
