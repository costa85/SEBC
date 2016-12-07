## Report the latest available version of the API
```
[root@clouderaseb00 cloudera-scm-agent]# curl -u costa85:cloudera 'http://clouderaseb00.gitcluster.com:7180/api/version'
v14
```

## Report the CM version
```
[root@clouderaseb00 cloudera-scm-agent]# curl -u costa85:cloudera 'http://clouderaseb00.gitcluster.com:7180/api/v13/cm/version'
{
  "version" : "5.9.0",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20161006-1801",
  "gitHash" : "898a5e032c080e18833dfc58180761f6ef2ea351",
  "snapshot" : false
}
```
## List all CM users
```
[root@clouderaseb00 cloudera-scm-agent]# curl -u costa85:cloudera 'http://clouderaseb00.gitcluster.com:7180/api/v13/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "costa85",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}
```

## Report the database server in use by CM
```

```