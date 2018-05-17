The command and output for hdfs dfs -ls /user
[ec2-user@ip-172-31-35-195 ~]$ hadoop fs -ls /user
Found 6 items
drwxr-xr-x   - beltran supergroup          0 2018-05-17 08:20 /user/beltran
drwxrwxrwx   - mapred  hadoop              0 2018-05-17 08:16 /user/history
drwxrwxr-t   - hive    hive                0 2018-05-17 08:17 /user/hive
drwxrwxr-x   - hue     hue                 0 2018-05-17 08:17 /user/hue
drwxr-xr-x   - jimenez supergroup          0 2018-05-17 08:20 /user/jimenez
drwxrwxr-x   - oozie   oozie               0 2018-05-17 08:18 /user/oozie


*
The command and output from the CM API call http://ec2-18-188-234-194.us-east-2.compute.amazonaws.com:7180/api/v18/hosts
{
  "items" : [ {
    "hostId" : "ffd46daf-21fd-4600-94a6-ba89b5746080",
    "ipAddress" : "172.31.35.15",
    "hostname" : "ip-172-31-35-15.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/hostRedirect/ffd46daf-21fd-4600-94a6-ba89b5746080",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656265216
  }, {
    "hostId" : "91ece9e2-1c5f-400b-891e-c68464c49840",
    "ipAddress" : "172.31.35.195",
    "hostname" : "ip-172-31-35-195.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/hostRedirect/91ece9e2-1c5f-400b-891e-c68464c49840",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656269312
  }, {
    "hostId" : "7a395d56-8e40-4ce1-8f0c-f000eb152250",
    "ipAddress" : "172.31.36.192",
    "hostname" : "ip-172-31-36-192.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/hostRedirect/7a395d56-8e40-4ce1-8f0c-f000eb152250",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656269312
  }, {
    "hostId" : "af8a3235-587d-46df-9179-0e8bc17c96dc",
    "ipAddress" : "172.31.38.16",
    "hostname" : "ip-172-31-38-16.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/hostRedirect/af8a3235-587d-46df-9179-0e8bc17c96dc",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656269312
  }, {
    "hostId" : "a44f8f0c-8014-4cb8-8767-e02938cdd2de",
    "ipAddress" : "172.31.46.211",
    "hostname" : "ip-172-31-46-211.us-east-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/hostRedirect/a44f8f0c-8014-4cb8-8767-e02938cdd2de",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 16656269312
  } ]
}

*
The command and output from the CM API call ../api/v11/clusters/<githubName>/services
http://ec2-18-188-234-194.us-east-2.compute.amazonaws.com:7180/api/v18/clusters/nithinraot/services

'''
{
  "items" : [ {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "roleInstancesUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/zookeeper/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/oozie",
    "roleInstancesUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/oozie/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/hue",
    "roleInstancesUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/hue/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HUE_LOAD_BALANCER_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "roleInstancesUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/hdfs/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/yarn",
    "roleInstancesUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/yarn/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hbase",
    "type" : "HBASE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/hbase",
    "roleInstancesUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/hbase/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HBASE_MASTER_HEALTH",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HBASE_REGION_SERVERS_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HBase",
    "entityStatus" : "GOOD_HEALTH"
  }, {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive",
    "roleInstancesUrl" : "http://ip-172-31-38-16.us-east-2.compute.internal:7180/cmf/serviceRedirect/hive/instances",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD",
      "suppressed" : false
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive",
    "entityStatus" : "GOOD_HEALTH"
  } ]
}'''