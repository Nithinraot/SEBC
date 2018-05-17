*T
he command hostname -f and its output
[root@ip-172-31-38-16 yum.repos.d]# hostname -f
ip-172-31-38-16.us-east-2.compute.internal

*
[root@ip-172-31-38-16 cloudera-scm-server]# mysql -u root -pCloudera -e "status;"
--------------
mysql  Ver 15.1 Distrib 5.5.56-MariaDB, for Linux (x86_64) using readline 5.1

Connection id:          374
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
Uptime:                 1 hour 20 min 58 sec

Threads: 9  Questions: 77560  Slow queries: 0  Opens: 693  Flush tables: 2  Open tables: 79  Queries per second avg: 15.965

*
The command mysql -u <user> -p<password> -e "show databases;" and its output
[root@ip-172-31-38-16 cloudera-scm-server]# mysql -u root -pCloudera -e "show databases;"
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

