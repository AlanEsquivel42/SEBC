```
[ec2-user@ip-172-31-9-209 ~]$ curl -u alanesquivel:cloudera http://54.174.227.211:7180/api/v16/cm/deployment > /home/ec2-user/deploylog
{
  "timestamp" : "2017-12-01T07:02:07.345Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "alanesquivel",
    "version" : "CDH5",
    "fullVersion" : "5.10.2",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-9-209.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive",
          "sensitive" : true
        }, {
          "name" : "hive_proxy_user_groups_list",
          "value" : "hive,hue,sentry",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "sentry_service",
          "value" : "sentry",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-03a264526b864a9b78911b97782ef836",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-4035116bcd12ff9dda7e566098d81eca",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-4035116bcd12ff9dda7e566098d81eca",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "437svnwgz3vhfvkrt3w6rzc3w",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-03a264526b864a9b78911b97782ef836",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6ikv796bntaak32kbkzlk74tg",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      }, {
        "name" : "hive-WEBHCAT-4035116bcd12ff9dda7e566098d81eca",
        "type" : "WEBHCAT",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_webhcat_secret_key",
            "value" : "c3hpptvkOA3YBP8iRqFB8c6qy2qUky",
            "sensitive" : true
          }, {
            "name" : "role_jceks_password",
            "value" : "c7qo7e2su43c5y4xf3hqom6m2",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-WEBHCAT-BASE"
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
            "name" : "hive_enable_db_notification",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "hive_metastore_java_heapsize",
            "value" : "6177161216",
            "sensitive" : false
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "617716121",
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
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_java_heapsize",
            "value" : "3918528512",
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
            "value" : "2164942438",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "364",
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
        "name" : "zookeeper-SERVER-000cb8e8b01bf0bda5878d308fa11772",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7s7iaz7at8vg8kbzinwzmjvql",
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
        "name" : "zookeeper-SERVER-03a264526b864a9b78911b97782ef836",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bp5fokngykvov8ae4ocea35im",
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
        "name" : "zookeeper-SERVER-4035116bcd12ff9dda7e566098d81eca",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8h884js5kwwl68lx1hava64qh",
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
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-9-209.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "database_password",
          "value" : "hue",
          "sensitive" : true
        }, {
          "name" : "database_type",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-03a264526b864a9b78911b97782ef836",
          "sensitive" : false
        }, {
          "name" : "oozie_service",
          "value" : "oozie",
          "sensitive" : false
        }, {
          "name" : "sentry_service",
          "value" : "sentry",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-4035116bcd12ff9dda7e566098d81eca",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6r2wvb0yh9ficv9ey3xcnmew0",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_LOAD_BALANCER-BASE"
        }
      }, {
        "name" : "hue-HUE_SERVER-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5q1npvsa5wzdte4h1iz6vlbif",
            "sensitive" : true
          }, {
            "name" : "secret_key",
            "value" : "msbcMfU3SBFp5jlxdZgqxkEznmOOBP",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      }, {
        "name" : "hue-HUE_SERVER-4035116bcd12ff9dda7e566098d81eca",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d2mol77khnwwlozpgf12isymv",
            "sensitive" : true
          }, {
            "name" : "secret_key",
            "value" : "4jhzEQJrXulnv7vEcfLBXax2EpOWnu",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      }, {
        "name" : "hue-KT_RENEWER-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7n7usql1l2366mt7o5cu0cwdx",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-KT_RENEWER-BASE"
        }
      }, {
        "name" : "hue-KT_RENEWER-4035116bcd12ff9dda7e566098d81eca",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4c7bb7r6txho01em55mpq9bqc",
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
        "name" : "oozie-OOZIE_SERVER-03a264526b864a9b78911b97782ef836",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6aebrods8k16d6kf7s8bsq06r",
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
            "value" : "ip-172-31-9-209.ec2.internal",
            "sensitive" : false
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie",
            "sensitive" : true
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql",
            "sensitive" : false
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie",
            "sensitive" : false
          } ]
        }
      } ]
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
          "value" : "ilTXif4GqSpStsKsfmUd3UYBM2J2iQ",
          "sensitive" : true
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2jycvo9dne9xf5anj5pewaj2c",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-03a264526b864a9b78911b97782ef836",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "74rtyuayrtp68e4ylb4h5bb9u",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-1"
        }
      }, {
        "name" : "yarn-NODEMANAGER-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "63obu3ub8ot61a4ff134khc4l",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-2"
        }
      }, {
        "name" : "yarn-NODEMANAGER-4035116bcd12ff9dda7e566098d81eca",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "10h04bvtx3red0757cd7a90sf",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "81",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "euou0ziuvfarudv4iualb983s",
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
            "value" : "12",
            "sensitive" : false
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1",
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
            "value" : "/data00/yarn/nm,/data01/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/data00/yarn/container-logs,/data01/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "6",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3528",
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
            "value" : "/data00/yarn/nm,/data01/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/data00/yarn/container-logs,/data01/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "7388",
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
            "value" : "/data00/yarn/nm,/data01/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/data00/yarn/container-logs,/data01/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "6994",
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
            "value" : "7388",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "6",
            "sensitive" : false
          } ]
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
          "value" : "5UDxz0qL3tpb8kUbWBHAedsn7PTamt",
          "sensitive" : true
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "wu62Jk99oL7ToYT7E4ijGP0LWmSqjg",
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
          "value" : "C3Q3o6dwTMG98Yq49ldFqqMVUpOPMT",
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
        "name" : "hdfs-BALANCER-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-03a264526b864a9b78911b97782ef836",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c1n81ab1xba3ifvq6nspwymkd",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3facn5jdvau4o8lkrknzb8l2k",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-4035116bcd12ff9dda7e566098d81eca",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "18b7tr4nn8uq2844i5ldk3ox7",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-03a264526b864a9b78911b97782ef836",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2s4vwmm5v65225uki6xw9kpge",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4unkpe7rujj5m6xvy1p6qoqzq",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-HTTPFS-03a264526b864a9b78911b97782ef836",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "exxggnz0jbz5k9ephlb8mm2r4",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-HTTPFS-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-03a264526b864a9b78911b97782ef836",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ceq7hz5u7m83lqdzh8vum0g9x",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d9qit5oxcc2f7u33xfr17ttln",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-4035116bcd12ff9dda7e566098d81eca",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4tw48vjvxwbyue57ht2c1x7i7",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-03a264526b864a9b78911b97782ef836",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "namenode_id",
            "value" : "88",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "9qa8pktsrx1oi0ywdu4g5xuzf",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "namenode_id",
            "value" : "83",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "1mg6c0esohpw4158x4z54gw94",
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
            "value" : "/data00/dfs/dn,/data01/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1",
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
            "value" : "/data00/dfs/jn",
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
            "value" : "/data00/dfs/nn,/data01/dfs/nn",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022",
            "sensitive" : false
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "3918528512",
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
            "value" : "/data00/dfs/snn",
            "sensitive" : false
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "3918528512",
            "sensitive" : false
          } ]
        }
      } ],
      "replicationSchedules" : [ ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-172-31-9-209.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "sentry_server_database_password",
          "value" : "sentry",
          "sensitive" : true
        }, {
          "name" : "sentry_service_admin_group",
          "value" : "hive,impala,hue,solr,kafka,example",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "sentry-GATEWAY-03a264526b864a9b78911b97782ef836",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "sentry-GATEWAY-BASE"
        }
      }, {
        "name" : "sentry-GATEWAY-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "sentry-GATEWAY-BASE"
        }
      }, {
        "name" : "sentry-GATEWAY-4035116bcd12ff9dda7e566098d81eca",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "sentry-GATEWAY-BASE"
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-000cb8e8b01bf0bda5878d308fa11772",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "32pc92rix0fpfk6un3p3h5xcs",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "sentry-SENTRY_SERVER-BASE"
        }
      } ],
      "displayName" : "Sentry",
      "roleConfigGroups" : [ {
        "name" : "sentry-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "sentry"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-BASE",
        "displayName" : "Sentry Server Default Group",
        "roleType" : "SENTRY_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "sentry"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.10.2-1.cdh5.10.2.p0.5",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.10.2-1.cdh5.10.2.p0.5",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ],
    "uuid" : "6c341a03-13a4-4a1d-9b49-b5c333f46be3"
  } ],
  "hosts" : [ {
    "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844",
    "ipAddress" : "172.31.20.9",
    "hostname" : "ip-172-31-20-9.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e",
    "ipAddress" : "172.31.6.221",
    "hostname" : "ip-172-31-6-221.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82",
    "ipAddress" : "172.31.8.216",
    "hostname" : "ip-172-31-8-216.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836",
    "ipAddress" : "172.31.9.209",
    "hostname" : "ip-172-31-9-209.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b59b838c6cbb5c99074703e96cd147ec3c6097e0ca59a13230b967bcb0ba0abe",
    "pwSalt" : -5656284282436450571,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "89e7e42f7c02ccfa930c3825600993f8803497d9a06b67c4e73ce8380706f8c9",
    "pwSalt" : 6013351890209048386,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-NAVIGATOR-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9ac189ac604580fd18d631515902d2b4ca776d415826c45938f12c49c55042fd",
    "pwSalt" : 7056723502230065182,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-NAVIGATORMETASERVER-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "ee68a336b246b71da0597a64bb3d9ef0561e0e00f0f2b8c668b6f75fb1ac0ae6",
    "pwSalt" : -592292857874432780,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "accebefe1dfa5c21c1177d564ed2ea82e784df5f223a4509aa56c56f61f6cd43",
    "pwSalt" : 7766515928710883994,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c1063ff421c2fd29f5119e3869d6d5d3b0d4f2da325b7fd51f20ae72d97dda63",
    "pwSalt" : -6398533251134587014,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "c8a8897072252971406662f309942a3a9fe27640c5509b3dcea9fc4820c60f5b",
    "pwSalt" : 7002215014025643091,
    "pwLogin" : true
  }, {
    "name" : "alanesquivel",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "3f89a5a20050286c4b1cbe593e6b248be7c61c61f12e137a0ec96f10cd955e8e",
    "pwSalt" : -6939508506408413986,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "dd461a27a7b33cae9b6a9dbf0f4107e6627684e5a6dc72f576785625bdd6204b",
    "pwSalt" : -2977783126877696356,
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
      "name" : "mgmt-ALERTPUBLISHER-000cb8e8b01bf0bda5878d308fa11772",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "ab8xq904ub1hsphbjap15jbmp",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-000cb8e8b01bf0bda5878d308fa11772",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "9x7j786qo2gbx1as44zcdcwj7",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-000cb8e8b01bf0bda5878d308fa11772",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5eq1cthr6jlqdumh2k3ikk252",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-NAVIGATOR-000cb8e8b01bf0bda5878d308fa11772",
      "type" : "NAVIGATOR",
      "hostRef" : {
        "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "63zy6w4jlmbw0qncdk2ezic2",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-NAVIGATOR-BASE"
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-000cb8e8b01bf0bda5878d308fa11772",
      "type" : "NAVIGATORMETASERVER",
      "hostRef" : {
        "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5sxfu776kmqtcfuq7bpz2of1z",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-NAVIGATORMETASERVER-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-000cb8e8b01bf0bda5878d308fa11772",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "62vo63ujsg2stu70b8l5qfq2r",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-000cb8e8b01bf0bda5878d308fa11772",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "adb51a6a-18db-4df2-92bd-6ec473c94836"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "b7xwh82w33r4xontfg8xdaxyj",
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
        "items" : [ {
          "name" : "navigator_database_host",
          "value" : "ip-172-31-9-209.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "navigator_database_password",
          "value" : "nav",
          "sensitive" : true
        } ]
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
        "items" : [ {
          "name" : "nav_metaserver_database_host",
          "value" : "ip-172-31-9-209.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "nav_metaserver_database_password",
          "value" : "navms",
          "sensitive" : true
        } ]
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
          "value" : "ip-172-31-9-209.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman",
          "sensitive" : true
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman",
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
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false",
      "sensitive" : false
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 16:50",
      "sensitive" : false
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAABDAAEAEEFMQU5FU1FVSVZFTC5DT00ADGNsb3VkZXJhLXNjbQAAAAFaHwTZAQAXABDJ2fRliteH7eqCfmWo8+tQAAAAAQ==",
      "sensitive" : true
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm@ALANESQUIVEL.COM",
      "sensitive" : false
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-9-209.ec2.internal",
      "sensitive" : false
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "arcfour-hmac",
      "sensitive" : false
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true",
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
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/",
      "sensitive" : false
    }, {
      "name" : "SECURITY_REALM",
      "value" : "ALANESQUIVEL.COM",
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
```
