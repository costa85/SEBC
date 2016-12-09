```
[root@clouderaseb02 orchard]# beeline
2016-12-09 21:24:53,672 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-trfixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://clouderaseb00.gitcluster.com:10000/default;principal=hicom@COSTA85.SG
scan complete in 2ms
Connecting to jdbc:hive2://clouderaseb00.gitcluster.com:10000/default;principal=hive/cCOSTA85.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://clouderaseb00.gitcluster.com:> show tables;
INFO  : Compiling command(queryId=hive_20161209212626_0f81f17e-50df-4df3-8489-1190c236
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:stzer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161209212626_0f81f17e-50df-4df3-848 0.683 seconds
INFO  : Executing command(queryId=hive_20161209212626_0f81f17e-50df-4df3-8489-1190c236
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209212626_0f81f17e-50df-4df3-848 0.265 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.335 seconds)
0: jdbc:hive2://clouderaseb00.gitcluster.com:> create role overload;
INFO  : Compiling command(queryId=hive_20161209212626_434d3dce-1462-4276-bcce-62416e8ed0d4): create role overload
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161209212626_434d3dce-1462-4276-bcce-62416e8ed0d4); Time taken: 0.092 seconds
INFO  : Executing command(queryId=hive_20161209212626_434d3dce-1462-4276-bcce-62416e8ed0d4): create role overload
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209212626_434d3dce-1462-4276-bcce-62416e8ed0d4); Time taken: 0.546 seconds
INFO  : OK
No rows affected (0.656 seconds)
0: jdbc:hive2://clouderaseb00.gitcluster.com:> GRANT ALL ON SERVER server1 TO ROLE overload;
INFO  : Compiling command(queryId=hive_20161209212727_b4dc476f-758b-44d0-bb86-b207a9405164): GRANT ALL ON SERVER server1 TO ROLE overload
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161209212727_b4dc476f-758b-44d0-bb86-b207a9405164); Time taken: 0.087 seconds
INFO  : Executing command(queryId=hive_20161209212727_b4dc476f-758b-44d0-bb86-b207a9405164): GRANT ALL ON SERVER server1 TO ROLE overload
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209212727_b4dc476f-758b-44d0-bb86-b207a9405164); Time taken: 0.084 seconds
INFO  : OK
No rows affected (0.187 seconds)
0: jdbc:hive2://clouderaseb00.gitcluster.com:> GRANT ROLE overload to group walks;
INFO  : Compiling command(queryId=hive_20161209212727_6f7a1e71-04fd-4cd5-b1a3-fb4bf3d9943e): GRANT ROLE overload to group walks
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20161209212727_6f7a1e71-04fd-4cd5-b1a3-fb4bf3d9943e); Time taken: 0.062 seconds
INFO  : Executing command(queryId=hive_20161209212727_6f7a1e71-04fd-4cd5-b1a3-fb4bf3d9943e): GRANT ROLE overload to group walks
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209212727_6f7a1e71-04fd-4cd5-b1a3-fb4bf3d9943e); Time taken: 0.071 seconds
INFO  : OK
No rows affected (0.152 seconds)
0: jdbc:hive2://clouderaseb00.gitcluster.com:> show tables;
INFO  : Compiling command(queryId=hive_20161209212727_f8cf10ff-bb3f-4886-b5f2-06b075af73af): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161209212727_f8cf10ff-bb3f-4886-b5f2-06b075af73af); Time taken: 0.064 seconds
INFO  : Executing command(queryId=hive_20161209212727_f8cf10ff-bb3f-4886-b5f2-06b075af73af): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209212727_f8cf10ff-bb3f-4886-b5f2-06b075af73af); Time taken: 0.13 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.26 seconds)
0: jdbc:hive2://clouderaseb00.gitcluster.com:>

```



```
[root@clouderaseb02 orchard]# kinit orchard
Password for orchard@COSTA85.SG:
[root@clouderaseb02 orchard]# beeline
2016-12-09 21:33:04,986 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-tree module jar containing PrefixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://clouderaseb00.gitcluster.com:10000/default;principal=hive/clouderaseb00.gitcluster.com@COSTA85.SG
scan complete in 2ms
Connecting to jdbc:hive2://clouderaseb00.gitcluster.com:10000/default;principal=hive/clouderaseb00.gitcluster.com@COSTA85.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://clouderaseb00.gitcluster.com:> show tables;
INFO  : Compiling command(queryId=hive_20161209213333_2d32927a-1c73-4639-bb49-d8b0d7e29845): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161209213333_2d32927a-1c73-4639-bb49-d8b0d7e29845); Time taken: 0.07 seconds
INFO  : Executing command(queryId=hive_20161209213333_2d32927a-1c73-4639-bb49-d8b0d7e29845): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209213333_2d32927a-1c73-4639-bb49-d8b0d7e29845); Time taken: 0.144 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.326 seconds)
0: jdbc:hive2://clouderaseb00.gitcluster.com:>

```


```
[root@clouderaseb02 orchard]# beeline
2016-12-09 21:34:28,033 WARN  [main] mapreduce.TableMapReduceUtil: The hbase-prefix-tree module jar containing PrefixTreeCodec is not present.  Continuing without it.
Beeline version 1.1.0-cdh5.9.0 by Apache Hive
beeline> !connect jdbc:hive2://clouderaseb00.gitcluster.com:10000/default;principal=hive/clouderaseb00.gitcluster.com@COSTA85.SG
scan complete in 2ms
Connecting to jdbc:hive2://clouderaseb00.gitcluster.com:10000/default;principal=hive/clouderaseb00.gitcluster.com@COSTA85.SG
Connected to: Apache Hive (version 1.1.0-cdh5.9.0)
Driver: Hive JDBC (version 1.1.0-cdh5.9.0)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://clouderaseb00.gitcluster.com:> show tables;
INFO  : Compiling command(queryId=hive_20161209213434_26ec41d3-c221-411a-b19a-1e8274467840): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20161209213434_26ec41d3-c221-411a-b19a-1e8274467840); Time taken: 0.062 seconds
INFO  : Executing command(queryId=hive_20161209213434_26ec41d3-c221-411a-b19a-1e8274467840): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20161209213434_26ec41d3-c221-411a-b19a-1e8274467840); Time taken: 0.125 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.317 seconds)
0: jdbc:hive2://clouderaseb00.gitcluster.com:>

```