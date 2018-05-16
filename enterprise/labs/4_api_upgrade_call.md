## <center> <a name="CM "/>  Upgrade Cloudera Manager
* Use the API on the command line to:
	* Report the latest available version of the API '''curl -X GET -u "admin:admin" 'http://ec2-18-191-111-190.us-east-2.compute.amazonaws.com:7180/api/version''''
	* Report the CM version -> '''curl -X GET -u "admin:admin" 'http://ec2-18-191-111-190.us-east-2.compute.amazonaws.com:7180/api/v19/cm/version''''
	* List all CM users -> '''http://ec2-18-191-111-190.us-east-2.compute.amazonaws.com:7180/api/v19/users'''
	* Report the database server in use by CM -> '''http://ec2-18-191-111-190.us-east-2.compute.amazonaws.com:7180/api/v19/cm/scmDbInfo'''