<<<<<<< HEAD

# Preguntas y respuestas
  
**What is ubertask optimization?**  
If the job is small, the application master may choose to run them in the same JVM as itself, since it judges the overhead of allocating new containers and running tasks in them as outweighing the gain to be had in running them in parallel, compared to running them sequentially on one node. (This is different to Mapreduce 1, where small jobs are never run on a single task tracker.)
  
**Where in CM is the Kerberos Security Realm value displayed?**  
1- Select Administration tab.  
2- Select Settings.  
3- Select Category > Kerberos.  
4- Select Status > Non-default  
  
**Which CDH service(s) host a property for enabling Kerberos authentication?**  
Sentry  
Hue  
Hive  
  
How do you upgrade the CM agents?  
1. Log in to the Cloudera Manager Admin Console.  
  
2. Upgrade hosts using one of the following methods:  
   + Cloudera Manager installs Agent software  
     -Select Yes, I would like to upgrade the Cloudera Manager Agent packages now and click Continue.  
Select the release of the Cloudera Manager Agent to install. Normally, this is the Matched Release for this Cloudera Manager Server. However, if you used a custom repository (instead of archive.cloudera.com) for the Cloudera Manager server, select Custom Repository and provide the required information. The custom repository allows you to use an alternative location, but that location must contain the matched Agent version.
Click Continue. The JDK Installation Options page displays.
Leave Install Oracle Java SE Development Kit (JDK) checked to allow Cloudera Manager to install the JDK on each cluster host, or uncheck if you plan to install it yourself.
If local laws permit you to deploy unlimited strength encryption, and you are running a secure cluster, check the Install Java Unlimited Strength Encryption Policy Files checkbox.
Click Continue.
Specify credentials and initiate Agent installation:
Select root or enter the username for an account that has password-less sudo permission.
Select an authentication method:
If you choose password authentication, enter and confirm the password.
If you choose public-key authentication, provide a passphrase and path to the required key files.
You can specify an alternate SSH port. The default value is 22.
You can specify the maximum number of host installations to run at once. The default value is 10.
Click Continue. The Cloudera Manager Agent packages and optionally the JDK are installed.
Click Continue. The Host Inspector runs to inspect your managed hosts for correct versions and configurations. If there are problems, you can make changes and then rerun the inspector. When you are satisfied with the inspection results, click Continue.


Give the tsquery statement used to chart Hue's CPU utilization?  
Name all the roles that make up the Hive service  
What steps must be completed before integrating Cloudera Manager with Kerberos?  


{
  "timestamp" : "2017-11-30T18:17:09.388Z",
  "clusters" : [ {
    "name" : "alanesquivel",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_enable_db_notification",
            "value" : "true"
          }, {
            "name" : "hive_metastore_java_heapsize",
            "value" : "6177161216"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "617716121"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false"
          }, {
            "name" : "hiveserver2_java_heapsize",
            "value" : "3918528512"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2164942438"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "364"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-9-209.ec2.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive"
        }, {
          "name" : "hive_proxy_user_groups_list",
          "value" : "hive,hue,sentry"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "sentry_service",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
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
        }
      }, {
        "name" : "hive-GATEWAY-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-4035116bcd12ff9dda7e566098d81eca",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ ]
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
            "value" : "a6takmqm5hm5mq24ui4xrlvke"
          } ]
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
            "value" : "7kqq7h9xsjhrk5x1tljgpm26a"
          } ]
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
            "value" : "c3hpptvkOA3YBP8iRqFB8c6qy2qUky"
          }, {
            "name" : "role_jceks_password",
            "value" : "a0zjr9sf0a5sshlhbd6m83dbc"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true"
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
            "value" : "ahb9rc8h1c956yzlnb5cidnk1"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
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
            "value" : "82xe2lzc8mye1hlkuw19f7l3o"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
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
            "value" : "6n6anr2g8a0j3ro1ooybzis2t"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-9-209.ec2.internal"
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
          "value" : "hdfs-HTTPFS-03a264526b864a9b78911b97782ef836"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "sentry_service",
          "value" : "sentry"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-4035116bcd12ff9dda7e566098d81eca",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "855ynzfr2nvq519okuzpdny2o"
          }, {
            "name" : "secret_key",
            "value" : "4jhzEQJrXulnv7vEcfLBXax2EpOWnu"
          } ]
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
            "value" : "6cxt6i82grz2uhry0y367amh9"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-9-209.ec2.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
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
        "name" : "oozie-OOZIE_SERVER-03a264526b864a9b78911b97782ef836",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "16f2c96e-0337-43da-a881-59e1d7b84b82"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5h293r9abqwftdq4nw2f2vdr5"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "12"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/data00/yarn/nm,/data01/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/data00/yarn/container-logs,/data01/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "6994"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "7388"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "6"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "ilTXif4GqSpStsKsfmUd3UYBM2J2iQ"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
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
            "value" : "4ukaxbrk643sx0ppozn0l5t32"
          } ]
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
            "value" : "4178d3mono56rse1mdm42zbf0"
          } ]
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
            "value" : "7yphmd2352hg24kd0eoprfusp"
          } ]
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
            "value" : "74192q6qgyjujo7qmofv5joh"
          } ]
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
            "value" : "81"
          }, {
            "name" : "role_jceks_password",
            "value" : "261lmcsjpbk9n08ufh5rxbczp"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/data00/dfs/dn,/data01/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700"
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1"
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400"
          }, {
            "name" : "rm_io_weight",
            "value" : "200"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/data00/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/data00/dfs/nn,/data01/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "3918528512"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/data00/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "3918528512"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding"
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "5UDxz0qL3tpb8kUbWBHAedsn7PTamt"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "wu62Jk99oL7ToYT7E4ijGP0LWmSqjg"
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos"
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "C3Q3o6dwTMG98Yq49ldFqqMVUpOPMT"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
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
            "value" : "6ytv0xqq40mqe36smj5g064ry"
          } ]
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
            "value" : "53n4jxy2qvnq1pgldjwwhefvy"
          } ]
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
            "value" : "e2bwst1w9q2fgkmhp133tn1p2"
          } ]
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
            "value" : "ep5xxh73vpr9yxz43yyz9k31o"
          } ]
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
            "value" : "8j4lndk9lj73adciep25s68t"
          } ]
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
            "value" : "ct3gdyv823cn8pt03m6wt5v2p"
          } ]
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
            "value" : "3vojnl9pabd8s68dnzw0b7p4k"
          } ]
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
            "value" : "e9zonfi5wgbeoe5gnkzrdybbr"
          } ]
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
            "value" : "4wuhjowk5x2l3woedovf1cawz"
          } ]
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
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "88"
          }, {
            "name" : "role_jceks_password",
            "value" : "ag73vs6t3rritqwtd2rqvl2im"
          } ]
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
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "83"
          }, {
            "name" : "role_jceks_password",
            "value" : "43s22hkmvpmqob0xpsg9esc8m"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-172-31-9-209.ec2.internal"
        }, {
          "name" : "sentry_server_database_password",
          "value" : "sentry"
        }, {
          "name" : "sentry_service_admin_group",
          "value" : "hive,impala,hue,solr,kafka,example"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
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
        }
      }, {
        "name" : "sentry-GATEWAY-29b14e44b87a9ce7dbe82a4ae4d27008",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1b06a444-55fe-4e15-986f-762f8d4a5844"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-GATEWAY-4035116bcd12ff9dda7e566098d81eca",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "9e2b7a86-9b33-4639-a752-6a3e4957c66e"
        },
        "config" : {
          "items" : [ ]
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
            "value" : "20w3fpomksbc6xcsh7uedkmg6"
          } ]
        }
      } ],
      "displayName" : "Sentry"
    } ]
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
    "pwHash" : "0db2a24c7f5c95810447a6ae9c2530ccc45cfff43055a0644cc5252081c7a66a",
    "pwSalt" : -9165919723721430293,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f9c74ea2958171c0fb6c73a0f56e634cc85ac5b312a9adc45a9ad4406f804c9c",
    "pwSalt" : -334239161097721894,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-NAVIGATOR-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f23db7d53a2167735a5bc4a062f587c3cb55f91e891eb975681f708aa374bd70",
    "pwSalt" : 2060255788325950126,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-NAVIGATORMETASERVER-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "205de21ab19a0a6ff3ed0e0b356733124c2ebf50434d8efb1b609c975a3552e9",
    "pwSalt" : -3058991207218824232,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "3021fa5f69ebc0eac78d8e3b4b80b71c4868bfea6c4ce8a9745c38e90a092b4b",
    "pwSalt" : -6279846300876898930,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-000cb8e8b01bf0bda5878d308fa11772",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "4710bee469e6ccf2841ebecb37fc2b4fa6c8f974a4173da5a4cc4de7bf1a1bfc",
    "pwSalt" : 7920590375028208495,
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
    "version" : "5.10.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170626-1942",
    "gitHash" : "15f547c8802e02d59901ee3fe1c5c5733eab0227",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "NAVIGATOR",
        "items" : [ {
          "name" : "navigator_database_host",
          "value" : "ip-172-31-9-209.ec2.internal"
        }, {
          "name" : "navigator_database_password",
          "value" : "nav"
        } ]
      }, {
        "roleType" : "NAVIGATORMETASERVER",
        "items" : [ {
          "name" : "nav_metaserver_database_host",
          "value" : "ip-172-31-9-209.ec2.internal"
        }, {
          "name" : "nav_metaserver_database_password",
          "value" : "navms"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-9-209.ec2.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
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
          "value" : "ezlm6brfhadxk8orjj2q3h9se"
        } ]
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
          "value" : "3jbzz9q0ialc4u7xg9j935hmb"
        } ]
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
          "value" : "7g5wbrih8eb3xc85a63yx6tg9"
        } ]
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
          "value" : "4q2idio16x9rj2fy6qxmsz8v5"
        } ]
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
          "value" : "a52zpm4rwku2v8bm01vf3wukx"
        } ]
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
          "value" : "87cudyly0sg0w5phjvohspmum"
        } ]
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
          "value" : "9bdcitjrzb4c9wd76i2aw02o9"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false"
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 16:50"
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAABDAAEAEEFMQU5FU1FVSVZFTC5DT00ADGNsb3VkZXJhLXNjbQAAAAFaHwTZAQAXABDJ2fRliteH7eqCfmWo8+tQAAAAAQ=="
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm@ALANESQUIVEL.COM"
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-9-209.ec2.internal"
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "arcfour-hmac"
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true"
    }, {
      "name" : "MAX_RENEW_LIFE",
      "value" : "604800"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    }, {
      "name" : "SECURITY_REALM",
      "value" : "ALANESQUIVEL.COM"
    } ]
  }
}
=======

# Preguntas y respuestas
  
**What is ubertask optimization?**  
If the job is small, the application master may choose to run them in the same JVM as itself, since it judges the overhead of allocating new containers and running tasks in them as outweighing the gain to be had in running them in parallel, compared to running them sequentially on one node. (This is different to Mapreduce 1, where small jobs are never run on a single task tracker.)
  
**Where in CM is the Kerberos Security Realm value displayed?**  
1- Select Administration tab.  
2- Select Settings.  
3- Select Category > Kerberos.  
4- Select Status > Non-default  
  
**Which CDH service(s) host a property for enabling Kerberos authentication?**  
Sentry  
Hue  
Hive  
HDFS  
Impala  
Solr  
Kafka  
  
**How do you upgrade the CM agents?**  
1. Log in to the Cloudera Manager Admin Console.  
  
2. Upgrade hosts using one of the following methods:  
   + Cloudera Manager installs Agent software  
      - Select Yes, I would like to upgrade the Cloudera Manager Agent packages now and click Continue.  
      - Select the release of the Cloudera Manager Agent to install. Normally, this is the Matched Release for this Cloudera Manager    
      Server. However, if you used a custom repository (instead of archive.cloudera.com) for the Cloudera Manager server, select Custom 
      Repository and provide the required information. The custom repository allows you to use an alternative location, but that 
      location must contain the matched Agent version.  
     - Click Continue. The JDK Installation Options page displays.  
        * Leave Install Oracle Java SE Development Kit (JDK) checked to allow Cloudera Manager to install the JDK on each cluster host,           or uncheck if you plan to install it yourself.
        * If local laws permit you to deploy unlimited strength encryption, and you are running a secure cluster, check the Install Java           Unlimited Strength Encryption Policy Files checkbox.
     Click Continue.
     - Specify credentials and initiate Agent installation:
       * Select root or enter the username for an account that has password-less sudo permission.
       * Select an authentication method:
          * If you choose password authentication, enter and confirm the password.
          * If you choose public-key authentication, provide a passphrase and path to the required key files.
       * You can specify an alternate SSH port. The default value is 22.
       * You can specify the maximum number of host installations to run at once. The default value is 10.
      - Click Continue. The Cloudera Manager Agent packages and optionally the JDK are installed.
        Click Continue. The Host Inspector runs to inspect your managed hosts for correct versions and configurations. If there are             problems, you can make changes and then rerun the inspector. When you are satisfied with the inspection results, click Continue.

**Give the tsquery statement used to chart Hue's CPU utilization?**  
    SELECT cpu_percent_across_hosts WHERE serviceType=HUE  
  
**Name all the roles that make up the Hive service**  
    - Hive Metastore Server
    - WebHCat Server
    - HiveServer2
    - Gateway


**What steps must be completed before integrating Cloudera Manager with Kerberos?**  
  
  To install packages for a Kerberos server:  
  <code>yum -y install krb5-server krb5-libs krb5-auth-dialog krb5-workstation</code>
  
  To install packages for a Kerberos client:  
  <code>yum -y install krb5-workstation krb5-libs krb5-auth-dialog</code>
  
  *Server
  
  <code># vim /var/kerberos/krb5kdc/kdc.conf</code>
  ```
[kdcdefaults]
 kdc_ports = 88
 kdc_tcp_ports = 88

[realms]
  ALANESQUIVEL.COM = {
  #master_key_type = aes256-cts
  acl_file = /var/kerberos/krb5kdc/kadm5.acl
  dict_file = /usr/share/dict/words
  admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
  supported_enctypes = aes256-cts:normal aes128-cts:normal des3-hmac-sha1:normal arcfour-hmac:normal des-hmac-sha1:normal des-cbc-md5:normal des-cbc-crc:normal
  max_life = 1d
  max_renewable_life = 7d
 }
 ```
 
 *All Clients
 
  <code># vim /etc/krb5.conf</code>
 ```
 
[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = ALANESQUIVEL.COM
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true
 udp_preference_limit = 1
 default_tgs_enctypes = arcfour-hmac
 default_tkt_enctypes = arcfour-hmac 

[realms] 
  ALANESQUIVEL.COM = {
  kdc = ip-172-31-9-209.ec2.internal
  admin_server = ip-172-31-9-209.ec2.internal
 }

[domain_realm]
   .ec2.internal.com = ALANESQUIVEL.COM
   ec2.internal.com = ALANESQUIVEL.COM
   ```
   
   *Create the database using the kdb5_util utility. (Server)
   
   <code># /usr/sbin/kdb5_util create -s</code>
   ``` 
   Loading random data
   Initializing database '/var/kerberos/krb5kdc/principal' for realm 'ALANESQUIVEL.COM',
   master key name 'K/M@ALANESQUIVEL.COM'
   You will be prompted for the database Master Password.
   It is important that you NOT FORGET this password.
   Enter KDC database master key:
   Re-enter KDC database master key to verify:
   ```
   
   *In Server, add cloudera-scm principal, it will be used by Cloudera Manager later to manage Hadoop principals.
  
   <code># kadmin.local</code>
   ```
   kadmin.local:  addprinc cloudera-scm@ALANESQUIVEL.COM
   WARNING: no policy specified for cloudera-scm@ALANESQUIVEL.COM; defaulting to no policy
   Enter password for principal "cloudera-scm@ALANESQUIVEL.COM":
   Re-enter password for principal "cloudera-scm@ALANESQUIVEL.COM":
   Principal "cloudera-scm@ALANESQUIVEL.COM" created.
   ```
   
   *Add */admin and cloudera-scm to ACL(Access Control List), which gives privilege to add principals for admin and cloudera-scm  
   principal
   
   <code># vim /var/kerberos/krb5kdc/kadm5.acl</code>  
   ``` 
    */admin@ALANESQUIVEL.COM *
    cloudera-scm@ALANESQUIVEL.COM admilc
   ```
   
   *Adds the password policy to the database.  
   
   <code># kadmin.local</code>
   ```
    kadmin.local:  addpol admin
    kadmin.local:  addpol users
    kadmin.local:  addpol hosts
    kadmin.local:  exit
   ```
   
   *Start Kerberos using the following commands:  
   
   <code>#service krb5kdc start</code>  
   <code>#service kadmin start</code>  
   
   
>>>>>>> e8d608ea6acdd1c45cbd91c92d9125ac45982531
