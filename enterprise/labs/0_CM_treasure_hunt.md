## <center> <a name="CM "/> CM_treasure_hunt
* What is ubertask optimization?
	Answer -> Whether to enable ubertask optimization, which runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings
* Where in CM is the Kerberos Security Realm value displayed?
	Answer -> under Administration -> settings -> Kerberos Security Realm
* Which CDH service(s) host a property for enabling Kerberos authentication?
* How do you upgrade the CM agents?
	Answer -> Log in to the Cloudera Manager Admin Console. The Upgrade Wizard displays.
* Give the tsquery statement used to chart Hue's CPU utilization?
	answer -> SELECT cpu_system_rate FROM REPORTS
* Name all the roles that make up the Hive service
	Answer -> hivemetastore server, hiverserver2, gateways
* What steps must be completed before integrating Cloudera Manager with Kerberos?
	Answer -> 
	* Set up a working KDC. Cloudera Manager supports authentication with MIT KDC and Active Directory
	* Configure the KDC to allow renewable tickets with non-zero ticket lifetimes.
	* If you are using Active Directory, make sure LDAP over TLS/SSL (LDAPS) is enabled for the Domain Controllers.
	* Install the OS-specific packages for your cluster listed in the table: like openldap-clients on the Cloudera Manager Server host & krb5-workstation, krb5-libs on ALL hosts
	* Create an account for Cloudera Manager that has the permissions to create other accounts in the KDC. 