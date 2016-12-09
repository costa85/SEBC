```
[root@clouderaseb02 ~]# hdfs dfs -ls /user
Found 7 items
drwxr-xr-x   - hdfs    hdfs             0 2016-12-09 20:18 /user/hdfs
drwxrwxrwx   - mapred  hadoop           0 2016-12-09 20:15 /user/history
drwxrwxr-t   - hive    hive             0 2016-12-09 20:16 /user/hive
drwxrwxr-x   - hue     hue              0 2016-12-09 20:17 /user/hue
drwxrwxr-x   - oozie   oozie            0 2016-12-09 20:17 /user/oozie
drwxr-xr-x   - orchard orchard          0 2016-12-09 20:19 /user/orchard
drwxr-xr-x   - raffles raffles          0 2016-12-09 20:19 /user/raffles
[root@clouderaseb02 ~]#
```






```
[root@clouderaseb02 ~]# curl -u admin:admin "clouderaseb01.gitcluster.com:7180/api/v14/hosts"
{
  "items" : [ {
    "hostId" : "567a3a14-e50b-473c-a985-2bbff088a26a",
    "ipAddress" : "172.16.31.20",
    "hostname" : "clouderaseb00.gitcluster.com",
    "rackId" : "/default",
    "hostUrl" : "http://clouderaseb01.gitcluster.com:7180/cmf/hostRedirect/567a3a14-e50b-473c-a985-2bbff088a26a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 25198514176
  }, {
    "hostId" : "b217a2f2-04fc-4fd0-9151-7ec0812f9af7",
    "ipAddress" : "172.16.31.21",
    "hostname" : "clouderaseb01.gitcluster.com",
    "rackId" : "/default",
    "hostUrl" : "http://clouderaseb01.gitcluster.com:7180/cmf/hostRedirect/b217a2f2-04fc-4fd0-9151-7ec0812f9af7",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 25198514176
  }, {
    "hostId" : "45e15b56-2f3a-49a7-a523-3ed666ef0970",
    "ipAddress" : "172.16.31.22",
    "hostname" : "clouderaseb02.gitcluster.com",
    "rackId" : "/default",
    "hostUrl" : "http://clouderaseb01.gitcluster.com:7180/cmf/hostRedirect/45e15b56-2f3a-49a7-a523-3ed666ef0970",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 16726073344
  }, {
    "hostId" : "461b44fb-c53b-4637-9a12-0d8d00184918",
    "ipAddress" : "172.16.31.23",
    "hostname" : "clouderaseb03.gitcluster.com",
    "rackId" : "/default",
    "hostUrl" : "http://clouderaseb01.gitcluster.com:7180/cmf/hostRedirect/461b44fb-c53b-4637-9a12-0d8d00184918",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 16726073344
  }, {
    "hostId" : "710933c5-350d-496c-9ab7-2bf2b6db4334",
    "ipAddress" : "172.16.31.24",
    "hostname" : "clouderaseb04.gitcluster.com",
    "rackId" : "/default",
    "hostUrl" : "http://clouderaseb01.gitcluster.com:7180/cmf/hostRedirect/710933c5-350d-496c-9ab7-2bf2b6db4334",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 16726073344
  } ]
[root@clouderaseb02 ~]#
```