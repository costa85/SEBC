# Use curl
```
[root@clouderaseb00 ~]# curl -u costa85:cloudera "http://clouderaseb00.gitcluster.com:7180/api/v13/cm/deployment" > cm-deployment.json
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 42824    0 42824    0     0   534k      0 --:--:-- --:--:-- --:--:--  543k
```


# Output
```
{
  "timestamp" : "2016-12-07T12:00:42.486Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "costa85",
    "version" : "CDH5",
    "fullVersion" : "5.8.2",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "clouderaseb00.gitcluster.com"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-748c15e6a1aae5c2979f1ecbc1d1d91e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-c77135eaeedfed3f4371bedccc6affda",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d3ir2kgztfjuaq5wg587f4ire"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-748c15e6a1aae5c2979f1ecbc1d1d91e",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1vhic2uqw0jig51hckfhujnyp"
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
            "value" : "420478976"
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
            "value" : "1334837248"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "1122133606"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "188"
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
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-7db6646004995025f25e76b74c75e7ba",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "30234301-f850-4c20-9249-f1c3569eb2af"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2f6gbsa71yiyv4ygazh5yc920"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-858cd4e43d2cbcba7603fd33ba764f24",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "abc89d56-b60a-4eb1-9b6d-152991b576f8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8iib0ru7usbti2tidq9ye9rds"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-8c6317bee016e3b0226b500e28306df5",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "4ee11aa5-c25a-4545-979b-5d4f61a34fc5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aiaycbvx2ejhuu3u34v2m7irg"
          }, {
            "name" : "serverId",
            "value" : "2"
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
            "name" : "zookeeper_server_java_heapsize",
            "value" : "1015021568"
          } ]
        }
      } ]
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "clouderaseb00.gitcluster.com"
        }, {
          "name" : "database_password",
          "value" : "hue"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-748c15e6a1aae5c2979f1ecbc1d1d91e"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-c77135eaeedfed3f4371bedccc6affda",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8b4i3e4qii39x5ysv4t2360op"
          }, {
            "name" : "secret_key",
            "value" : "zJt6RCsann5QHk4jMbes80f4P2ydk4"
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
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-c77135eaeedfed3f4371bedccc6affda",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7hig2cvgfbt01ac2yyty75iom"
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
            "value" : "clouderaseb00.gitcluster.com"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "420478976"
          } ]
        }
      } ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "8xVLg5vH1dNczzcTyt5hsDUgtt3CQa"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-c77135eaeedfed3f4371bedccc6affda",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7gdq7m6ixn5ewg91zv5ihg2ie"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-7db6646004995025f25e76b74c75e7ba",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "30234301-f850-4c20-9249-f1c3569eb2af"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bgtdmfphjgznpajv2638c9e2i"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-858cd4e43d2cbcba7603fd33ba764f24",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "abc89d56-b60a-4eb1-9b6d-152991b576f8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cn6d5fz8uu9alavjol7b396xh"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-8c6317bee016e3b0226b500e28306df5",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "4ee11aa5-c25a-4545-979b-5d4f61a34fc5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5afyow1u2m9ua31r55pfuhkey"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-c77135eaeedfed3f4371bedccc6affda",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "42"
          }, {
            "name" : "role_jceks_password",
            "value" : "2jf03nhf0s2tsr6d66sp4zwal"
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
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
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
            "value" : "420478976"
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
            "name" : "node_manager_java_heapsize",
            "value" : "1015021568"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/data1/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "1024"
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
            "value" : "420478976"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "1024"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "2JvhGuJpmb5Fxez8paqLGCCXAjupbi"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "dfs_permissions",
          "value" : "false"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "Bu3e4dQgvWjZfIudZNF7d591W0zimx"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "wexxNomgxC3rAgVLTrRStjX7Cp7QIv"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-748c15e6a1aae5c2979f1ecbc1d1d91e",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-7db6646004995025f25e76b74c75e7ba",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "30234301-f850-4c20-9249-f1c3569eb2af"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "72r8582g375bghr1lmuzmgtdi"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-858cd4e43d2cbcba7603fd33ba764f24",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "abc89d56-b60a-4eb1-9b6d-152991b576f8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "clv2d1j2pwm0o0kchdirl150d"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-8c6317bee016e3b0226b500e28306df5",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "4ee11aa5-c25a-4545-979b-5d4f61a34fc5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "f29ccekxjfjzg7leb91l1h53h"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-748c15e6a1aae5c2979f1ecbc1d1d91e",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bqcvhud3z12xieth8unjrfo9r"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-c77135eaeedfed3f4371bedccc6affda",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6rtpczaygiwj4kw4nnkinq2ul"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-GATEWAY-748c15e6a1aae5c2979f1ecbc1d1d91e",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-GATEWAY-BASE"
        }
      }, {
        "name" : "hdfs-GATEWAY-7db6646004995025f25e76b74c75e7ba",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "30234301-f850-4c20-9249-f1c3569eb2af"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-GATEWAY-BASE"
        }
      }, {
        "name" : "hdfs-GATEWAY-858cd4e43d2cbcba7603fd33ba764f24",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "abc89d56-b60a-4eb1-9b6d-152991b576f8"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-GATEWAY-BASE"
        }
      }, {
        "name" : "hdfs-GATEWAY-8c6317bee016e3b0226b500e28306df5",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "4ee11aa5-c25a-4545-979b-5d4f61a34fc5"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-GATEWAY-BASE"
        }
      }, {
        "name" : "hdfs-GATEWAY-c77135eaeedfed3f4371bedccc6affda",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-GATEWAY-BASE"
        }
      }, {
        "name" : "hdfs-HTTPFS-748c15e6a1aae5c2979f1ecbc1d1d91e",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1mcy6zrmbne780qowdq5ahqlm"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-HTTPFS-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-748c15e6a1aae5c2979f1ecbc1d1d91e",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7ekkzmbpx3zte6q20clffqlo6"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-858cd4e43d2cbcba7603fd33ba764f24",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "abc89d56-b60a-4eb1-9b6d-152991b576f8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6f7eccadktdb2sbcb3f3tqr1b"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-c77135eaeedfed3f4371bedccc6affda",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8i168t84ugx31j6a5ls0oztdb"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-748c15e6a1aae5c2979f1ecbc1d1d91e",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "44"
          }, {
            "name" : "role_jceks_password",
            "value" : "2cpmvh1n1npqre21da3d6y8p1"
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-c77135eaeedfed3f4371bedccc6affda",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "49"
          }, {
            "name" : "role_jceks_password",
            "value" : "dw15zqz4sh2nliepuzi56tgxc"
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
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/data1/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "10555414937"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
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
            "value" : "true"
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
            "value" : "/var/dfs/jn"
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
            "value" : "/data1/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
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
            "value" : "/data1/dfs/snn"
          } ]
        }
      } ],
      "replicationSchedules" : [ {
        "id" : 7,
        "startTime" : "2016-12-06T16:01:12.775Z",
        "interval" : 0,
        "intervalUnit" : "MINUTE",
        "paused" : false,
        "nextRun" : null,
        "alertOnStart" : false,
        "alertOnSuccess" : false,
        "alertOnFail" : false,
        "alertOnAbort" : false,
        "hdfsArguments" : {
          "sourceService" : {
            "peerName" : "einsamkeid",
            "clusterName" : "cluster",
            "serviceName" : "hdfs"
          },
          "sourcePath" : "/user/hdfs/source",
          "destinationPath" : "/user/costa85/repl_data",
          "mapreduceServiceName" : "yarn",
          "dryRun" : false,
          "abortOnError" : false,
          "removeMissingFiles" : false,
          "preserveReplicationCount" : true,
          "preserveBlockSize" : true,
          "preservePermissions" : true,
          "skipChecksumChecks" : false,
          "skipTrash" : false,
          "replicationStrategy" : "DYNAMIC",
          "preserveXAttrs" : false,
          "exclusionFilters" : [ ]
        },
        "active" : false
      } ],
      "snapshotPolicies" : [ {
        "name" : "sebc-hdfs-test",
        "hourlySnapshots" : 1,
        "dailySnapshots" : 0,
        "weeklySnapshots" : 0,
        "monthlySnapshots" : 0,
        "yearlySnapshots" : 0,
        "minuteOfHour" : 45,
        "hourOfDay" : 0,
        "dayOfWeek" : 1,
        "dayOfMonth" : 1,
        "monthOfYear" : 1,
        "hoursForHourlySnapshots" : [ ],
        "alertOnStart" : false,
        "alertOnSuccess" : false,
        "alertOnFail" : true,
        "alertOnAbort" : false,
        "paused" : false,
        "hdfsArguments" : {
          "pathPatterns" : [ "/user/hdfs/precious" ]
        },
        "lastCommand" : {
          "id" : 785,
          "name" : "HdfsScheduledSnapshotsCommand",
          "startTime" : "2016-12-07T11:45:00.016Z",
          "endTime" : "2016-12-07T11:45:18.705Z",
          "active" : false,
          "success" : true,
          "resultMessage" : "Successfully created/deleted snapshots as per snapshot policy sebc-hdfs-test.",
          "resultDataUrl" : "/cmf/command/785/download",
          "serviceRef" : {
            "clusterName" : "cluster",
            "serviceName" : "hdfs"
          },
          "hdfsResult" : {
            "processedPathCount" : 1,
            "unprocessedPathCount" : 0,
            "createdSnapshotCount" : 1,
            "deletedSnapshotCount" : 1,
            "creationErrorCount" : 0,
            "deletionErrorCount" : 0
          }
        },
        "lastSuccessfulCommand" : {
          "id" : 785,
          "name" : "HdfsScheduledSnapshotsCommand",
          "startTime" : "2016-12-07T11:45:00.016Z",
          "endTime" : "2016-12-07T11:45:18.705Z",
          "active" : false,
          "success" : true,
          "resultMessage" : "Successfully created/deleted snapshots as per snapshot policy sebc-hdfs-test.",
          "resultDataUrl" : "/cmf/command/785/download",
          "serviceRef" : {
            "clusterName" : "cluster",
            "serviceName" : "hdfs"
          },
          "hdfsResult" : {
            "processedPathCount" : 1,
            "unprocessedPathCount" : 0,
            "createdSnapshotCount" : 1,
            "deletedSnapshotCount" : 1,
            "creationErrorCount" : 0,
            "deletionErrorCount" : 0
          }
        }
      } ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.8.2-1.cdh5.8.2.p0.3",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.8.2-1.cdh5.8.2.p0.3",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082",
    "ipAddress" : "172.16.31.20",
    "hostname" : "clouderaseb00.gitcluster.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "280c5e6c-1c52-43eb-b33d-99a318e95f9c",
    "ipAddress" : "172.16.31.21",
    "hostname" : "clouderaseb01.gitcluster.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ {
        "name" : "memory_overcommit_threshold",
        "value" : "0.95"
      } ]
    }
  }, {
    "hostId" : "abc89d56-b60a-4eb1-9b6d-152991b576f8",
    "ipAddress" : "172.16.31.22",
    "hostname" : "clouderaseb02.gitcluster.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "30234301-f850-4c20-9249-f1c3569eb2af",
    "ipAddress" : "172.16.31.23",
    "hostname" : "clouderaseb03.gitcluster.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "4ee11aa5-c25a-4545-979b-5d4f61a34fc5",
    "ipAddress" : "172.16.31.24",
    "hostname" : "clouderaseb04.gitcluster.com",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-c77135eaeedfed3f4371bedccc6affda",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f4710f72a849526498906a7369ad1d1dbc8c33816f1da49c6f271e9668dee7e5",
    "pwSalt" : 7643092126571002449,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-c77135eaeedfed3f4371bedccc6affda",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "10e66fb0eea82d9b868cdca5874ef7711020b7317c8eea153285debe35064546",
    "pwSalt" : -6887615344775799788,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-c77135eaeedfed3f4371bedccc6affda",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e9d09b167313435f0496cce727e1c72767b3dd4c94d0de0dd176e2f368472c99",
    "pwSalt" : 4650055557421078937,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-c77135eaeedfed3f4371bedccc6affda",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "2e468a9bd02585ad48acc367e5b52b2165b1720bdbec4a7a2a4790b714712746",
    "pwSalt" : 987344333150519183,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "cce130aedbc16d6f741e58da3f85739806d7e8ce77c539816e6a4f5fd9c69f6f",
    "pwSalt" : -8066424281002335133,
    "pwLogin" : true
  }, {
    "name" : "costa85",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "6005dcc89a5f2908175e64e4b624376ccf371182c582d3411b5fb87d76fc2784",
    "pwSalt" : -4072181113803748792,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "866f690ed85e20e83eab8f9127993406744b0cd2790e56ff5bbbfb85901d5109",
    "pwSalt" : -5424650254413059931,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20160916-1426",
    "gitHash" : "d23c620f3a3bbd85d8511d6ebba49beaaab14b75",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-c77135eaeedfed3f4371bedccc6affda",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8k7kfllmgzz3ntf0k93p6x7ie"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-c77135eaeedfed3f4371bedccc6affda",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "69r1apyxfhl3tk4dxxmfoqyt4"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-c77135eaeedfed3f4371bedccc6affda",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "cve6n4mqejmn7izt33ghkb56y"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-c77135eaeedfed3f4371bedccc6affda",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a5qo3b4ni7racwxwq4d2sg9ts"
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-c77135eaeedfed3f4371bedccc6affda",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "2367807e-3034-4f06-9d96-98b817e8e082"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6961x3luo7lq761hkl78cqiqy"
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
        "items" : [ ]
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
          "value" : "420478976"
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
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
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
          "value" : "clouderaseb00.gitcluster.com"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "420478976"
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
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 14:00"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "NOT_ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://172.16.31.20/cdh5.8.2,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  },
  "allHostsConfig" : {
    "items" : [ {
      "name" : "rm_enabled",
      "value" : "true"
    } ]
  },
  "peers" : [ {
    "name" : "einsamkeid",
    "type" : "REPLICATION",
    "url" : "http://ec2-54-254-214-41.ap-southeast-1.compute.amazonaws.com:7180",
    "username" : "__cloudera_internal_user__c938f140-bd43-4304-ba04-094da2257811",
    "password" : "ca9e1a10-fffc-4e58-9d17-47daacd7072a7c7955fe-3f46-4c4d-bbec-19b3c4dd68c5",
    "clouderaManagerCreatedUser" : true
  } ],
  "hostTemplates" : {
    "items" : [ ]
  }
}
```