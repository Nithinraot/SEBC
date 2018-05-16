## <center> <a name="CM "/> 

http://ec2-18-191-111-190.us-east-2.compute.amazonaws.com:7180/api/v19/cm/deployment
'''json
{
  "timestamp" : "2018-05-16T21:28:04.349Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "SEBC",
    "version" : "CDH5",
    "fullVersion" : "5.14.2",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9ag7425r7iidjam9hdr8bgkb6",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "3",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-a3f3dbf2a4986250b3e39a1c87fe0963",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "1b1fabcb-1b04-4e36-9653-2bf1ffc03ccc"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3wd6ke294gctje512g8p66f38",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "1",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-b2df43a065959c6fae14fc8790b024e3",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "c228ce63-48da-4105-83c1-6cee533d029a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "92qcldm6c0iqekyvsqhlphyog",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "2",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      } ],
      "displayName" : "ZooKeeper",
      "roleConfigGroups" : [ {
        "name" : "zookeeper-SERVER-BASE",
        "displayName" : "Server Default Group",
        "roleType" : "SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "zookeeper"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4s4sookww6o7wvvdm116dpnll",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
        }
      } ],
      "displayName" : "Oozie",
      "roleConfigGroups" : [ {
        "name" : "oozie-OOZIE_SERVER-BASE",
        "displayName" : "Oozie Server Default Group",
        "roleType" : "OOZIE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "oozie"
        },
        "config" : {
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-5-153.us-east-2.compute.internal",
            "sensitive" : false
          }, {
            "name" : "oozie_database_password",
            "value" : "oozieuser",
            "sensitive" : true
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql",
            "sensitive" : false
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie",
            "sensitive" : false
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "745537536",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-5-153.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "database_name",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "database_password",
          "value" : "Cloudera",
          "sensitive" : true
        }, {
          "name" : "database_type",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "database_user",
          "value" : "root",
          "sensitive" : false
        }, {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-48afbfe3a4234620ffbf4413f0b2db3c",
          "sensitive" : false
        }, {
          "name" : "oozie_service",
          "value" : "oozie",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-b2df43a065959c6fae14fc8790b024e3",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "c228ce63-48da-4105-83c1-6cee533d029a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d8a4vmr21rlppc9tvx2okssah",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_LOAD_BALANCER-BASE"
        }
      }, {
        "name" : "hue-HUE_SERVER-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "845201db-b26e-47bd-abf2-b925438faf7e",
            "sensitive" : true
          }, {
            "name" : "role_jceks_password",
            "value" : "1qqopu131tdm3jr82qeimjwjc",
            "sensitive" : true
          }, {
            "name" : "secret_key",
            "value" : "wvprfc8LLn63q2IWLe4jIr4M9c8MwR",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      }, {
        "name" : "hue-KT_RENEWER-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "21zi8cnzw3jo30ljums6tvutq",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-KT_RENEWER-BASE"
        }
      } ],
      "displayName" : "Hue",
      "roleConfigGroups" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-BASE",
        "displayName" : "Load Balancer Default Group",
        "roleType" : "HUE_LOAD_BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-HUE_SERVER-BASE",
        "displayName" : "Hue Server Default Group",
        "roleType" : "HUE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-KT_RENEWER-BASE",
        "displayName" : "Kerberos Ticket Renewer Default Group",
        "roleType" : "KT_RENEWER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding",
          "sensitive" : false
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "l24V4y8pgam6JClUibZOOLRhbgJeKR",
          "sensitive" : true
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "lxnfMXO4HO93GpEd2hSo4D4Zv5lgK6",
          "sensitive" : true
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos",
          "sensitive" : false
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "M3SrN1El5PiB9ASUwbEiScSRk0rIDZ",
          "sensitive" : true
        }, {
          "name" : "rm_dirty",
          "value" : "false",
          "sensitive" : false
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-96d832c4028511db9406570ad6c67a4f",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "ff68b7c8-ce38-462f-b085-4e2c8c2d27a1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8mu4ax8sgeez91mcrq1ijqszb",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-3"
        }
      }, {
        "name" : "hdfs-DATANODE-a3f3dbf2a4986250b3e39a1c87fe0963",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "1b1fabcb-1b04-4e36-9653-2bf1ffc03ccc"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "233kh2lztql4n2sp83f19zfgl",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-b2df43a065959c6fae14fc8790b024e3",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "c228ce63-48da-4105-83c1-6cee533d029a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ee55wiqhqux99eoqhjk45158b",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-1"
        }
      }, {
        "name" : "hdfs-DATANODE-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "crn819j9gfh8i2h1alsub04u",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-2"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "259objpzp33gmuchj1xohuia0",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-96d832c4028511db9406570ad6c67a4f",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "ff68b7c8-ce38-462f-b085-4e2c8c2d27a1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9n4t1w7m9vhm0pzsw7kp5llf2",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a7y08gp12xgcjz6av12d4omq3",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-96d832c4028511db9406570ad6c67a4f",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "ff68b7c8-ce38-462f-b085-4e2c8c2d27a1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4gx4aneyklzbkvqu9aomgzre3",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8mfmqcg86ezio6l8y3890oqv",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "sebcnameservice1",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "sebcnameservice1",
            "sensitive" : false
          }, {
            "name" : "namenode_id",
            "value" : "84",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "6r8bdixrli19p1rvj27owz8af",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-96d832c4028511db9406570ad6c67a4f",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "ff68b7c8-ce38-462f-b085-4e2c8c2d27a1"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "sebcnameservice1",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "sebcnameservice1",
            "sensitive" : false
          }, {
            "name" : "namenode_id",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "2axej329ytzm3fxdq82a9bf3e",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      } ],
      "displayName" : "HDFS",
      "roleConfigGroups" : [ {
        "name" : "hdfs-BALANCER-BASE",
        "displayName" : "Balancer Default Group",
        "roleType" : "BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-1",
        "displayName" : "DataNode Group 1",
        "roleType" : "DATANODE",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824",
            "sensitive" : false
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3219965132",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004",
            "sensitive" : false
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400",
            "sensitive" : false
          }, {
            "name" : "rm_io_weight",
            "value" : "200",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-2",
        "displayName" : "DataNode Group 2",
        "roleType" : "DATANODE",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824",
            "sensitive" : false
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3219965132",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-3",
        "displayName" : "DataNode Group 3",
        "roleType" : "DATANODE",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824",
            "sensitive" : false
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3219965132",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-BASE",
        "displayName" : "DataNode Default Group",
        "roleType" : "DATANODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824",
            "sensitive" : false
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3219965132",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
        "displayName" : "Failover Controller Default Group",
        "roleType" : "FAILOVERCONTROLLER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-BASE",
        "displayName" : "HttpFS Default Group",
        "roleType" : "HTTPFS",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-BASE",
        "displayName" : "JournalNode Default Group",
        "roleType" : "JOURNALNODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-BASE",
        "displayName" : "NameNode Default Group",
        "roleType" : "NAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022",
            "sensitive" : false
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "2700083200",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-BASE",
        "displayName" : "NFS Gateway Default Group",
        "roleType" : "NFSGATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-BASE",
        "displayName" : "SecondaryNameNode Default Group",
        "roleType" : "SECONDARYNAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn",
            "sensitive" : false
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "2700083200",
            "sensitive" : false
          } ]
        }
      } ],
      "replicationSchedules" : [ ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "rm_dirty",
          "value" : "false",
          "sensitive" : false
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80",
          "sensitive" : false
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false",
          "sensitive" : false
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false",
          "sensitive" : false
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "U2MnKSV5MadqUioNTvDkImfXkdqiZ9",
          "sensitive" : true
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3epjkhcxkpwc3ogtaqoqw076u",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-96d832c4028511db9406570ad6c67a4f",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "ff68b7c8-ce38-462f-b085-4e2c8c2d27a1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "36gk40d6if937lbu82x6fc72s",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-a3f3dbf2a4986250b3e39a1c87fe0963",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "1b1fabcb-1b04-4e36-9653-2bf1ffc03ccc"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "nbiji3403sfnxcp3ih22ug5c",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-1"
        }
      }, {
        "name" : "yarn-NODEMANAGER-b2df43a065959c6fae14fc8790b024e3",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "c228ce63-48da-4105-83c1-6cee533d029a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "kd19on6hlmrpzsfnhhly4rfq",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-2"
        }
      }, {
        "name" : "yarn-NODEMANAGER-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2f8vu85a75vhvy9yjehnnq0ne",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-3"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "91",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "arafkg8f5wwayq4di31yayn8r",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
        }
      } ],
      "displayName" : "YARN (MR2 Included)",
      "roleConfigGroups" : [ {
        "name" : "yarn-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8",
            "sensitive" : false
          }, {
            "name" : "mapred_submit_replication",
            "value" : "3",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-BASE",
        "displayName" : "JobHistory Server Default Group",
        "roleType" : "JOBHISTORY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1",
        "displayName" : "NodeManager Group 1",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1600",
            "sensitive" : false
          }, {
            "name" : "rm_io_weight",
            "value" : "800",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "4618",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-2",
        "displayName" : "NodeManager Group 2",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1543",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-3",
        "displayName" : "NodeManager Group 3",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "node_manager_java_heapsize",
            "value" : "745537536",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1024",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-BASE",
        "displayName" : "NodeManager Default Group",
        "roleType" : "NODEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1603",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-BASE",
        "displayName" : "ResourceManager Default Group",
        "roleType" : "RESOURCEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "4618",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-5-153.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hiveuser",
          "sensitive" : true
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-96d832c4028511db9406570ad6c67a4f",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "ff68b7c8-ce38-462f-b085-4e2c8c2d27a1"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-a3f3dbf2a4986250b3e39a1c87fe0963",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b1fabcb-1b04-4e36-9653-2bf1ffc03ccc"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-b2df43a065959c6fae14fc8790b024e3",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "c228ce63-48da-4105-83c1-6cee533d029a"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "59y6yls5akl21iqc5gkfvn9d1",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ch9t7baqy0p7z5ira9f4rbljj",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-1"
        }
      }, {
        "name" : "hive-HIVESERVER2-b2df43a065959c6fae14fc8790b024e3",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "c228ce63-48da-4105-83c1-6cee533d029a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1xahfo52h2ixfb9xk2071yv7u",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      } ],
      "displayName" : "Hive",
      "roleConfigGroups" : [ {
        "name" : "hive-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-BASE",
        "displayName" : "Hive Metastore Server Default Group",
        "roleType" : "HIVEMETASTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "745537536",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-1",
        "displayName" : "HiveServer2 Group 1",
        "roleType" : "HIVESERVER2",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2976907264",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "912680550",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "153",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-BASE",
        "displayName" : "HiveServer2 Default Group",
        "roleType" : "HIVESERVER2",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2273312768",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "912680550",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "153",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-BASE",
        "displayName" : "WebHCat Server Default Group",
        "roleType" : "WEBHCAT",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "replicationSchedules" : [ ]
    }, {
      "name" : "impala",
      "type" : "IMPALA",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "llama_am_ha_zk_auth_secret_key",
          "value" : "eMf1A09PdUjg2VPsTJnpXytdGQ12Ej",
          "sensitive" : true
        }, {
          "name" : "rm_dirty",
          "value" : "true",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "impala-CATALOGSERVER-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "CATALOGSERVER",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6aw3dmof12o930jrgzqgsuy3n",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "impala-CATALOGSERVER-BASE"
        }
      }, {
        "name" : "impala-IMPALAD-96d832c4028511db9406570ad6c67a4f",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "ff68b7c8-ce38-462f-b085-4e2c8c2d27a1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bjaip4w420295z5i19oepijvw",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "impala-IMPALAD-BASE"
        }
      }, {
        "name" : "impala-IMPALAD-a3f3dbf2a4986250b3e39a1c87fe0963",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "1b1fabcb-1b04-4e36-9653-2bf1ffc03ccc"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "17mcyhwr2sn153wwqe3jtb7ut",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "impala-IMPALAD-BASE"
        }
      }, {
        "name" : "impala-IMPALAD-b2df43a065959c6fae14fc8790b024e3",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "c228ce63-48da-4105-83c1-6cee533d029a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2wp7o3eqgtg64qv9cd2ozgr5x",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "impala-IMPALAD-BASE"
        }
      }, {
        "name" : "impala-IMPALAD-bdaf6cbd8a6c79918ca4fdea3da815d1",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "atr5uzmpw3h5rhkxq9bms8rm6",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "impala-IMPALAD-BASE"
        }
      }, {
        "name" : "impala-STATESTORE-48afbfe3a4234620ffbf4413f0b2db3c",
        "type" : "STATESTORE",
        "hostRef" : {
          "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "56oibzmt582zljfpzub2mbbwh",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "impala-STATESTORE-BASE"
        }
      } ],
      "displayName" : "Impala",
      "roleConfigGroups" : [ {
        "name" : "impala-CATALOGSERVER-BASE",
        "displayName" : "Impala Catalog Server Default Group",
        "roleType" : "CATALOGSERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "impala"
        },
        "config" : {
          "items" : [ {
            "name" : "catalogd_embedded_jvm_heapsize",
            "value" : "52428800",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-BASE",
        "displayName" : "Impala Daemon Default Group",
        "roleType" : "IMPALAD",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "impala"
        },
        "config" : {
          "items" : [ {
            "name" : "impalad_memory_limit",
            "value" : "268435456",
            "sensitive" : false
          }, {
            "name" : "scratch_dirs",
            "value" : "/impala/impalad",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "impala-LLAMA-BASE",
        "displayName" : "Impala Llama ApplicationMaster Default Group",
        "roleType" : "LLAMA",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "impala"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "impala-STATESTORE-BASE",
        "displayName" : "Impala StateStore Default Group",
        "roleType" : "STATESTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "impala"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    } ],
    "parcels" : [ {
      "product" : "KUDU",
      "version" : "1.4.0-1.cdh5.12.2.p0.8",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.14.2-1.cdh5.14.2.p0.3",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.14.2-1.cdh5.14.2.p0.3",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ],
    "uuid" : "0df36f34-b3cf-4728-bae0-abfa7770b14e"
  } ],
  "hosts" : [ {
    "hostId" : "c228ce63-48da-4105-83c1-6cee533d029a",
    "ipAddress" : "172.31.13.13",
    "hostname" : "ip-172-31-13-13.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a",
    "ipAddress" : "172.31.5.153",
    "hostname" : "ip-172-31-5-153.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "62a5f20c-9814-46ec-8187-0d99eeb82e8f",
    "ipAddress" : "172.31.6.251",
    "hostname" : "ip-172-31-6-251.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "1b1fabcb-1b04-4e36-9653-2bf1ffc03ccc",
    "ipAddress" : "172.31.8.213",
    "hostname" : "ip-172-31-8-213.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "ff68b7c8-ce38-462f-b085-4e2c8c2d27a1",
    "ipAddress" : "172.31.9.2",
    "hostname" : "ip-172-31-9-2.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-bdaf6cbd8a6c79918ca4fdea3da815d1",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "a5dd9d70f759f6e40275ff3d8da42c20e9a228e128c52c480131a1781913365e",
    "pwSalt" : 5788089310432740793,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-bdaf6cbd8a6c79918ca4fdea3da815d1",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c322fd593cee280bacfa7a91ae26f3f8e77cbd158d811b97fea5179ff8e37792",
    "pwSalt" : -6507610815616010578,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-bdaf6cbd8a6c79918ca4fdea3da815d1",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "a3925eef4b02e9055786df1be18ea47ef1d96ebb98016c8ffdbe43138ba8aea0",
    "pwSalt" : -1861462150169020569,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-bdaf6cbd8a6c79918ca4fdea3da815d1",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "65a4ef0ee04d3b299c0330f6d962ddefe0dca88cb1e6474450aa3abce9fc354b",
    "pwSalt" : 1034946894854311654,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-bdaf6cbd8a6c79918ca4fdea3da815d1",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "1b3815a940d11beb2b0824199a6582ff90e70e88091a4c36874c6206bfae9b91",
    "pwSalt" : 2702677990225080921,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-bdaf6cbd8a6c79918ca4fdea3da815d1",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "350bce48f61b05a8cf2c50c407507b0c4105335cbc57ed4a13c93d1f6cca38ef",
    "pwSalt" : 2337908361053657678,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "02f563a51552e9a1632beb57a57235499fe8bdba825ab47da135e66490405d64",
    "pwSalt" : 2345310225583184891,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "087347f9799a5cc52657fd01590442acc342c93ca48e42f5b8c0f5b83388be91",
    "pwSalt" : 502576401618074104,
    "pwLogin" : true
  }, {
    "name" : "nithinraot",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "c53eb1857b08a3d5681ce1a56f9c3de4cd064fbca92007f0f35a44e77669a12f",
    "pwSalt" : 3139805098218573398,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.14.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20180414-0409",
    "gitHash" : "7f2725eea4edeb1d184a2888db790d332167b6f8",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-bdaf6cbd8a6c79918ca4fdea3da815d1",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_database_name",
          "value" : "amon",
          "sensitive" : false
        }, {
          "name" : "firehose_database_password",
          "value" : "amonuser",
          "sensitive" : true
        }, {
          "name" : "firehose_database_user",
          "value" : "amon",
          "sensitive" : false
        }, {
          "name" : "role_jceks_password",
          "value" : "cguc15qnna5ezn27e4az9wu4c",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ACTIVITYMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-bdaf6cbd8a6c79918ca4fdea3da815d1",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "aio5pmaax2ffovq8b6981nyhk",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-bdaf6cbd8a6c79918ca4fdea3da815d1",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4ys4hy2hsjn1a3ohclg4jip4g",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-bdaf6cbd8a6c79918ca4fdea3da815d1",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a6eufb6s527ng383xy48eit6d",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-bdaf6cbd8a6c79918ca4fdea3da815d1",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a96eck1qa3a9pzwvk97ij5dk5",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-bdaf6cbd8a6c79918ca4fdea3da815d1",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "a5e8a32e-99d8-4b60-ba4d-6cc2f459a38a"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "ctfogy4wclnijt3fkb6x91y4",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
      }
    } ],
    "displayName" : "Cloudera Management Service",
    "roleConfigGroups" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-BASE",
      "displayName" : "Activity Monitor Default Group",
      "roleType" : "ACTIVITYMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-172-31-5-153.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "firehose_database_name",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "firehose_database_password",
          "value" : "Cloudera",
          "sensitive" : true
        }, {
          "name" : "firehose_database_user",
          "value" : "root",
          "sensitive" : false
        }, {
          "name" : "firehose_heapsize",
          "value" : "745537536",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-BASE",
      "displayName" : "Alert Publisher Default Group",
      "roleType" : "ALERTPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-BASE",
      "displayName" : "Event Server Default Group",
      "roleType" : "EVENTSERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "745537536",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-BASE",
      "displayName" : "Host Monitor Default Group",
      "roleType" : "HOSTMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "745537536",
          "sensitive" : false
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "968884224",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-BASE",
      "displayName" : "Navigator Audit Server Default Group",
      "roleType" : "NAVIGATOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
      "displayName" : "Navigator Metadata Server Default Group",
      "roleType" : "NAVIGATORMETASERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-BASE",
      "displayName" : "Reports Manager Default Group",
      "roleType" : "REPORTSMANAGER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-5-153.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_name",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_password",
          "value" : "Cloudera",
          "sensitive" : true
        }, {
          "name" : "headlamp_database_user",
          "value" : "root",
          "sensitive" : false
        }, {
          "name" : "headlamp_heapsize",
          "value" : "745537536",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-BASE",
      "displayName" : "Service Monitor Default Group",
      "roleType" : "SERVICEMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "745537536",
          "sensitive" : false
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "968884224",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-TELEMETRYPUBLISHER-BASE",
      "displayName" : "Telemetry Publisher Default Group",
      "roleType" : "TELEMETRYPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false",
      "sensitive" : false
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/21/2012 11:30",
      "sensitive" : false
    }, {
      "name" : "KDC_ADMIN_HOST",
      "value" : "ip-172-31-5-153.us-east-2.compute.internal",
      "sensitive" : false
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAABCAAIACENMT1VERVJBAAxjbG91ZGVyYS1zY20ABWFkbWluAAAAAVr7838BABcAEHDh02B0nXLwS43h5FT0AOUAAAABAAAAUgACAAhDTE9VREVSQQAMY2xvdWRlcmEtc2NtAAVhZG1pbgAAAAFa+/N/AQASACAeYtHTaCQTU7b8yBY3xjkWWtbN22ecOdQfWfwhcTyq0QAAAAEAAABCAAIACENMT1VERVJBAAxjbG91ZGVyYS1zY20ABWFkbWluAAAAAVr7838BABEAED5hg7YDRqwB4bjaLvej0HgAAAAB",
      "sensitive" : true
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm/admin@CLOUDERA",
      "sensitive" : false
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-5-153.us-east-2.compute.internal:880",
      "sensitive" : false
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "rc4-hmac aes256-cts aes128-cts",
      "sensitive" : false
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true",
      "sensitive" : false
    }, {
      "name" : "KRB_TICKET_LIFETIME",
      "value" : "604800",
      "sensitive" : false
    }, {
      "name" : "MAX_RENEW_LIFE",
      "value" : "604800",
      "sensitive" : false
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD",
      "sensitive" : false
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://ec2-18-220-231-157.us-east-2.compute.amazonaws.com/cm/kudu/parcels/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/",
      "sensitive" : false
    }, {
      "name" : "SECURITY_REALM",
      "value" : "CLOUDERA",
      "sensitive" : false
    } ]
  },
  "allHostsConfig" : {
    "items" : [ {
      "name" : "rm_enabled",
      "value" : "true",
      "sensitive" : false
    } ]
  },
  "peers" : [ ],
  "hostTemplates" : {
    "items" : [ ]
  }
}
'''