<div style="page-break-after: always;"></div>

* Setting up CM

* Installation pre-requisite.
	* check vm.swappiness on all your nodes
	* Show the mount attributes of your volume(s)
	* If you have ext-based volumes, list the reserve space setting
	* XFS volumes do not support reserve space
	* Disable transparent hugepage support
	* List your network interface configuration
	* Show that forward and reverse host lookups are correctly resolved
	* Show the nscd service is running
	* Show the ntpd service is running

* Installing Maria-dB

* Installing Java

* Installing CM

## <center> Installation Pre-requisite </center>

* swappiness -> sysctl -a |grep swappiness -> 1
* Nothing to be done for EXT, as my dev mount point is of type xfs
* mount volume -> [ec2-user@ip-172-31-5-153 ~]$ df -h
* huge page compaction disabling ->
	* echo 'never' > /sys/kernel/mm/transparent_hugepage/enabled
	* echo 'never' > /sys/kernel/mm/transparent_hugepage/defrag
	* cat enabled always madvise [never]
	* cat defrag always madvise [never]
* List your network interface configuration -> ifconfig
* Forward and reverse look up -> nslookup 172-31-6-251 & nslookup ip-172-31-6-251.us-east-2.compute.internal
* Install nscd & NTPD ->
	*yum install bind-utils
	*yum install nscd
	*yum install ntp
	*systemctl start ntpd
	*systemctl enable ntpd
	*systemctl enable status
	*systemctl status ntpd
* setting up /etc/hosts -> cat /etc/nsswitch.conf | grep hosts - Nothing modified as nsswitch takes care of this. cat /etc/hosts


## <center> Installation Maria-DB </center>
* sudo yum install mariadb-server
* sudo service mariadb stop
* update the /etc/my.cnf file
* sudo systemctl enable mariadb
* sudo service mariadb start
* sudo /usr/bin/mysql_secure_installation -> here set the username password for root/ create a DB named SCM & user named SCM where cloudera-manager-server will use this db.
* get the mysql-connector -> wget "https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.46.tar.gz"
* copy this connector to /user/share/java ( create this folder if it doesn not exists) -> cp mysql-connector-java-5.1.46 /user/share/java/mysql-connector-java

## <center> Installation Java </center>
* wget "http://archive.cloudera.com/director/redhat/7/x86_64/director/cloudera-director.repo"
* yum list all | grep oracle-* -> yum install oracle-j2sdk1.8.x86_64
* yum install oracle-j2sdk1.8.x86_64
* set home path,
	* export JAVA_HOME=/usr/java/jdk1.8.0_121-cloudera
	* export JRE_HOME=/usr/java/jdk1.8.0_121-cloudera/jre
	* export PATH=/usr/java/jdk1.8.0_121-cloudera/bin/:/usr/java/jdk1.8.0_121-cloudera/jre/bin/

## <center> Installation CM </center>
* wget https://archive.cloudera.com/cm5/redhat/7/x86_64/cm/cloudera-manager.repo
* yum list all | grep cloudera-manager
* yum install cloudera-manager-server
* Test the DB connection & also check if the required tables are created - > sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-5-153 scm scm
* If the above test succeeds then run systemctl start cloudera-scm-server

