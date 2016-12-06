
## Create a precious directory in HDFS; copy the ZIP course file into it.
```
[root@clouderaseb02 ~]# sudo -u hdfs hadoop fs -ls
Found 2 items
drwxr-xr-x   - hdfs hdfs          0 2016-12-06 07:17 .Trash
drwxr-xr-x   - hdfs hdfs          0 2016-12-06 21:45 precious
[root@clouderaseb02 ~]# sudo -u hdfs hadoop fs -ls precious
Found 1 items
-rw-r--r--   3 hdfs hdfs     410040 2016-12-06 21:37 precious/SEBC-master.zip
```

## Enable snapshots for precious
![](https://github.com/costa85/SEBC/blob/master/storage/labs/enablesnapshot.png)


## Create a snapshot called sebc-hdfs-test
![](https://github.com/costa85/SEBC/blob/master/storage/labs/SnapshotPolicy.png)

* snapshot run

![](https://github.com/costa85/SEBC/blob/master/storage/labs/SnapshotPolicy2.png)

## Delete the directory & Delete the ZIP file
```
[root@clouderaseb02 ~]# sudo -u hdfs hadoop fs -rm -R precious
rm: Failed to move to trash: hdfs://nameservice1/user/hdfs/precious: The directory /user/hdfs/precious cannot be deleted since /user/hdfs/precious is snapshottable and already has snapshots
[root@clouderaseb02 ~]# sudo -u hdfs hadoop fs -rm -R precious/SEBC-master.zip
16/12/06 21:55:21 INFO fs.TrashPolicyDefault: Moved: 'hdfs://nameservice1/user/hdfs/precious/SEBC-master.zip' to trash at: hdfs://nameservice1/user/hdfs/.Trash/Current/user/hdfs/precious/SEBC-master.zip
[root@clouderaseb02 ~]# sudo -u hdfs hadoop fs -ls precious
[root@clouderaseb02 ~]#
```

## Restore the deleted file
![](https://github.com/costa85/SEBC/blob/master/storage/labs/restoresnapshot.png)

* Restore File

![](https://github.com/costa85/SEBC/blob/master/storage/labs/restoresnapshot2.png)
