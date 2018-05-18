## <center> Deployment details

http://ec2-18-216-145-220.us-east-2.compute.amazonaws.com:7180/api/v16/cm/deployment

{
  "timestamp" : "2018-05-18T04:43:26.323Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "nithinraot",
    "version" : "CDH5",
    "fullVersion" : "5.11.2",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-46b48501af0c55202dacd836ca7f5f82",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "16f0uqslrzscqcegoewlo7iic",
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
        "name" : "zookeeper-SERVER-a1a996e28acf18c42e19b9299d65ab7f",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "700167ea-5468-47e8-bd40-8d17a534923a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cj04shgrdoz52eb60zjcug0w6",
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
      }, {
        "name" : "zookeeper-SERVER-f98bc7e383a63bb330411353192282ce",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "57931c69-d329-4c78-8a89-9ee5134dd950"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aef25ka0hm2wmcoy4rw6515gy",
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
          "items" : [ {
            "name" : "maxSessionTimeout",
            "value" : "60000",
            "sensitive" : false
          }, {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "406847488",
            "sensitive" : false
          } ]
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
        "name" : "oozie-OOZIE_SERVER-46b48501af0c55202dacd836ca7f5f82",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eyx2oizo66znzvcsreyyedlve",
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
            "value" : "ip-172-31-25-114.us-east-2.compute.internal",
            "sensitive" : false
          }, {
            "name" : "oozie_database_password",
            "value" : "Cloudera",
            "sensitive" : true
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql",
            "sensitive" : false
          }, {
            "name" : "oozie_database_user",
            "value" : "scm",
            "sensitive" : false
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "406847488",
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
          "value" : "ip-172-31-25-114.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "database_name",
          "value" : "oozie",
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
          "value" : "scm",
          "sensitive" : false
        }, {
          "name" : "hbase_service",
          "value" : "hbase",
          "sensitive" : false
        }, {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-46b48501af0c55202dacd836ca7f5f82",
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
        "name" : "hue-HUE_SERVER-46b48501af0c55202dacd836ca7f5f82",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eh5mywomppzy7k0kbzn84xosp",
            "sensitive" : true
          }, {
            "name" : "secret_key",
            "value" : "YC1vCBEHdk0jagi6sX46dbPDpA6opG",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
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
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "Qwpznx9kwRxHaKB2NXCwfDoHAueojQ",
          "sensitive" : true
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "ztzxD0sIPAEYdiTSC1ezAEtGpPxCfC",
          "sensitive" : true
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "UkoVgypUPZBMETc8EbpKvD3Z1UmV9O",
          "sensitive" : true
        }, {
          "name" : "rm_dirty",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-46b48501af0c55202dacd836ca7f5f82",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-24d92c0987ca2970d9415205cf1ec4ab",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "89e678b4-5f52-4969-bc1d-bf2a005a54e3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1437tw7n7si48nb8iaudeh4bx",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-a1a996e28acf18c42e19b9299d65ab7f",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "700167ea-5468-47e8-bd40-8d17a534923a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c9evmmhm5gmqgyb7620l0fg79",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-ec2e21775d01e5773600f766a30c5e17",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "d01a3a86-46cc-417f-9ff1-bb57a8ad37d5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4308gh7epldzaeh0yk0aibash",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-f98bc7e383a63bb330411353192282ce",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "57931c69-d329-4c78-8a89-9ee5134dd950"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dkwheoqw7scf23pipktg7mxpf",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-46b48501af0c55202dacd836ca7f5f82",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "namenode_id",
            "value" : "45",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "exb2eydhajgmbr0m54i41s45j",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-46b48501af0c55202dacd836ca7f5f82",
        "type" : "SECONDARYNAMENODE",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "99llwr2llx5uqk6ci3z85yqz6",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-SECONDARYNAMENODE-BASE"
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
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "406847488",
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
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "5367448780",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "3153068032",
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
          "items" : [ ]
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
            "value" : "406847488",
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
            "value" : "406847488",
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
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "mOoHqDzrpdX4vXwglFnmDciGsEtTCQ",
          "sensitive" : true
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-46b48501af0c55202dacd836ca7f5f82",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b179a7b8xxku8vtr27rzni6fm",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-24d92c0987ca2970d9415205cf1ec4ab",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "89e678b4-5f52-4969-bc1d-bf2a005a54e3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9o0otzqrlkalgh3ca7033p3n",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-a1a996e28acf18c42e19b9299d65ab7f",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "700167ea-5468-47e8-bd40-8d17a534923a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3fvut3jaonvjjm2eyea86xgub",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-ec2e21775d01e5773600f766a30c5e17",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "d01a3a86-46cc-417f-9ff1-bb57a8ad37d5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5z94gvhtfbi5ivtjx8z1qeff3",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-f98bc7e383a63bb330411353192282ce",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "57931c69-d329-4c78-8a89-9ee5134dd950"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2qkcgl08b8v2vi1fp9h87ec0i",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-46b48501af0c55202dacd836ca7f5f82",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "52",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "9m4a74mn8ekjnd5bw6rk7my46",
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
            "value" : "2",
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
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "406847488",
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
            "value" : "3007",
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
            "name" : "resource_manager_java_heapsize",
            "value" : "406847488",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3007",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hbase",
      "type" : "HBASE",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "rm_dirty",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hbase-MASTER-46b48501af0c55202dacd836ca7f5f82",
        "type" : "MASTER",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c3vtgutehde5l1vmky9jkuk9e",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-MASTER-BASE"
        }
      }, {
        "name" : "hbase-REGIONSERVER-24d92c0987ca2970d9415205cf1ec4ab",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "89e678b4-5f52-4969-bc1d-bf2a005a54e3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "129g9t4n433x8ke3zbpm13gll",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-REGIONSERVER-BASE"
        }
      }, {
        "name" : "hbase-REGIONSERVER-a1a996e28acf18c42e19b9299d65ab7f",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "700167ea-5468-47e8-bd40-8d17a534923a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "91cemyauid8fjko0w95l9tpjn",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-REGIONSERVER-BASE"
        }
      }, {
        "name" : "hbase-REGIONSERVER-ec2e21775d01e5773600f766a30c5e17",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "d01a3a86-46cc-417f-9ff1-bb57a8ad37d5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "deamp64yia8v4abhp354n7ews",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-REGIONSERVER-BASE"
        }
      }, {
        "name" : "hbase-REGIONSERVER-f98bc7e383a63bb330411353192282ce",
        "type" : "REGIONSERVER",
        "hostRef" : {
          "hostId" : "57931c69-d329-4c78-8a89-9ee5134dd950"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4r848b9qh0ebhifcp6eu04stg",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hbase-REGIONSERVER-BASE"
        }
      } ],
      "displayName" : "HBase",
      "roleConfigGroups" : [ {
        "name" : "hbase-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hbase-HBASERESTSERVER-BASE",
        "displayName" : "HBase REST Server Default Group",
        "roleType" : "HBASERESTSERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hbase-HBASETHRIFTSERVER-BASE",
        "displayName" : "HBase Thrift Server Default Group",
        "roleType" : "HBASETHRIFTSERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hbase-MASTER-BASE",
        "displayName" : "Master Default Group",
        "roleType" : "MASTER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ {
            "name" : "hbase_master_java_heapsize",
            "value" : "406847488",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hbase-REGIONSERVER-BASE",
        "displayName" : "RegionServer Default Group",
        "roleType" : "REGIONSERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hbase"
        },
        "config" : {
          "items" : [ {
            "name" : "hbase_regionserver_java_heapsize",
            "value" : "2425356288",
            "sensitive" : false
          } ]
        }
      } ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hbase_service",
          "value" : "hbase",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-25-114.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "Cloudera",
          "sensitive" : true
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "scm",
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
        "name" : "hive-GATEWAY-24d92c0987ca2970d9415205cf1ec4ab",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "89e678b4-5f52-4969-bc1d-bf2a005a54e3"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-46b48501af0c55202dacd836ca7f5f82",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-a1a996e28acf18c42e19b9299d65ab7f",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "700167ea-5468-47e8-bd40-8d17a534923a"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-ec2e21775d01e5773600f766a30c5e17",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d01a3a86-46cc-417f-9ff1-bb57a8ad37d5"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-f98bc7e383a63bb330411353192282ce",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "57931c69-d329-4c78-8a89-9ee5134dd950"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-46b48501af0c55202dacd836ca7f5f82",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "69z9ggnav0gkwxhokjfhe76be",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-46b48501af0c55202dacd836ca7f5f82",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1zvt1xqtqh6vjjtc2857mfrwy",
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
            "value" : "406847488",
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
            "value" : "406847488",
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
            "value" : "2680107827",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "451",
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
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.11.2-1.cdh5.11.2.p0.4",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.11.2-1.cdh5.11.2.p0.4",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ],
    "uuid" : "f34c2f8b-d042-40f4-8c03-dc332960030a"
  } ],
  "hosts" : [ {
    "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418",
    "ipAddress" : "172.31.20.193",
    "hostname" : "ip-172-31-20-193.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "700167ea-5468-47e8-bd40-8d17a534923a",
    "ipAddress" : "172.31.24.103",
    "hostname" : "ip-172-31-24-103.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "57931c69-d329-4c78-8a89-9ee5134dd950",
    "ipAddress" : "172.31.25.114",
    "hostname" : "ip-172-31-25-114.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "d01a3a86-46cc-417f-9ff1-bb57a8ad37d5",
    "ipAddress" : "172.31.28.168",
    "hostname" : "ip-172-31-28-168.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "89e678b4-5f52-4969-bc1d-bf2a005a54e3",
    "ipAddress" : "172.31.31.10",
    "hostname" : "ip-172-31-31-10.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-46b48501af0c55202dacd836ca7f5f82",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "5152417932839148cc6aa9e82c9b1aef196c57b3ddc718bc822a2e5c89c5c12f",
    "pwSalt" : -1572457092839442988,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-46b48501af0c55202dacd836ca7f5f82",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9a2ea35bf613a7da571d971dfd4e79a0127dbb0b38119f3f0c3d78472e1477f5",
    "pwSalt" : -2975248994962589217,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-46b48501af0c55202dacd836ca7f5f82",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9ee03930e9c1f4bc8cc3a3acfcc610bed70afb11818d7ff86a34e0ee0ef6bddb",
    "pwSalt" : -3863335567984621636,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-46b48501af0c55202dacd836ca7f5f82",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "4da91ffdd035c26f69f710ba2eacb68b10efaaa6ffd9060fc80e6cfb232e8461",
    "pwSalt" : -1713163840533454641,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "de0d7320831fdb5539775f700900e8557267fee6d6fbd6badab809aceb482348",
    "pwSalt" : -6415126453700408459,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.11.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170811-0014",
    "gitHash" : "3c3ea33a12076fb83a8f11c4452c52fac685d01b",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-46b48501af0c55202dacd836ca7f5f82",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bsf7zqm4ob39r9ta3bz8gqnog",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ACTIVITYMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-46b48501af0c55202dacd836ca7f5f82",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4guco9z10l9xr9zs7vmn7akle",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-46b48501af0c55202dacd836ca7f5f82",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4gfaptimkxnh9qzrfebfiji1r",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-46b48501af0c55202dacd836ca7f5f82",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5i9puvc1sfxg8amthvd73wcwb",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-46b48501af0c55202dacd836ca7f5f82",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "7ac9408f-83c3-40c8-a11c-1c0565f2f418"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "atgzmekonjbbcirdhph8ryiy",
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
          "value" : "ip-172-31-25-114.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "firehose_database_name",
          "value" : "rman",
          "sensitive" : false
        }, {
          "name" : "firehose_database_password",
          "value" : "Cloudera",
          "sensitive" : true
        }, {
          "name" : "firehose_database_user",
          "value" : "scm",
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
        "items" : [ ]
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
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736",
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
        "items" : [ ]
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
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736",
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
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 20:10",
      "sensitive" : false
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD",
      "sensitive" : false
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/",
      "sensitive" : false
    } ]
  },
  "allHostsConfig" : {
    "items" : [ ]
  },
  "peers" : [ ],
  "hostTemplates" : {
    "items" : [ ]
  }
}