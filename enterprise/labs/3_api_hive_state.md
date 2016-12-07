# Hive Stop

```
[root@clouderaseb00 ~]# curl -X POST -u costa85:cloudera "http://clouderaseb00.gitcluster.com:7180/api/v13/clusters/cluster/services/hive/commands/stop"
{
  "id" : 798,
  "name" : "Stop",
  "startTime" : "2016-12-07T13:21:34.289Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@clouderaseb00 ~]# curl -u costa85:cloudera 'http://clouderaseb00.gitcluster.com:7180/api/v13/commands/798'
{
  "id" : 798,
  "name" : "Stop",
  "startTime" : "2016-12-07T13:21:34.289Z",
  "endTime" : "2016-12-07T13:21:46.251Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully stopped service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 800,
      "name" : "Stop",
      "startTime" : "2016-12-07T13:21:34.292Z",
      "endTime" : "2016-12-07T13:21:46.249Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-748c15e6a1aae5c2979f1ecbc1d1d91e"
      }
    }, {
      "id" : 799,
      "name" : "Stop",
      "startTime" : "2016-12-07T13:21:34.291Z",
      "endTime" : "2016-12-07T13:21:36.319Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-c77135eaeedfed3f4371bedccc6affda"
      }
    } ]
  },
  "canRetry" : false
}[root@clouderaseb00 ~]#
```

# Hive Start

```
[root@clouderaseb00 ~]# curl -X POST -u costa85:cloudera "http://clouderaseb00.gitcluster.com:7180/api/v13/clusters/cluster/services/hive/commands/start"
{
  "id" : 802,
  "name" : "Start",
  "startTime" : "2016-12-07T13:25:57.110Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@clouderaseb00 ~]# curl u costa85:cloudera 'http://clouderaseb00.gitcluster.com:7180/api/v13/commands/802'
{
  "id" : 802,
  "name" : "Start",
  "startTime" : "2016-12-07T13:25:57.110Z",
  "endTime" : "2016-12-07T13:26:19.562Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully started service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 804,
      "name" : "Start",
      "startTime" : "2016-12-07T13:25:57.181Z",
      "endTime" : "2016-12-07T13:26:19.560Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-748c15e6a1aae5c2979f1ecbc1d1d91e"
      }
    }, {
      "id" : 803,
      "name" : "Start",
      "startTime" : "2016-12-07T13:25:57.131Z",
      "endTime" : "2016-12-07T13:26:19.558Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-c77135eaeedfed3f4371bedccc6affda"
      }
    } ]
  },
  "canRetry" : false
}[root@clouderaseb00 ~]#

```