## <center> <a name="CM "/>  Use the API
* Write curl statements that stop, start, and check the current state of your Hive service.
	* check the hive services using '''<http://ec2-18-191-111-190.us-east-2.compute.amazonaws.com:7180/api/v19/clusters/cluster/services/hive/>'''
	* Now run the curl command to stop the service -> '''<curl -u 'admin:admin' -X POST 'http://ec2-18-191-111-190.us-east-2.compute.amazonaws.com:7180/api/v19/clusters/cluster/services/hive/commands/stop'>'''
	* Now run the status command to check the status -> '''<curl -u admin:admin 'http://localhost:7180/api/v1/commands/1283'>'''
	* Now again run the start command to start the hive service -> '''<curl -u 'admin:admin' -X POST 'http://ec2-18-191-111-190.us-east-2.compute.amazonaws.com:7180/api/v19/clusters/cluster/services/hive/commands/start'>'''