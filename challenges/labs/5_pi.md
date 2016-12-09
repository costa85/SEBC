```
[orchard@clouderaseb02 ~]$ kinit orchard
Password for orchard@COSTA85.SG:
[orchard@clouderaseb02 ~]$ ll
total 140
-rw-r--r-- 1 orchard root 142551 Dec  9 21:04 hadoop-examples.jar
[orchard@clouderaseb02 ~]$ hadoop jar hadoop-examples.jar pi 10 100
Number of Maps  = 10
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Wrote input for Map #4
Wrote input for Map #5
Wrote input for Map #6
Wrote input for Map #7
Wrote input for Map #8
Wrote input for Map #9
Starting Job
16/12/09 21:07:39 INFO client.RMProxy: Connecting to ResourceManager at clouderaseb00.gitcluster.com/172.16.31.20:8032
16/12/09 21:07:39 INFO hdfs.DFSClient: Created token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@COSTA85.SG, renewer=yarn, realUser=, issueDate=1481285259349, maxDate=1481890059349, sequenceNumber=2, masterKeyId=2 on 172.16.31.20:8020
16/12/09 21:07:39 INFO security.TokenCache: Got dt for hdfs://clouderaseb00.gitcluster.com:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.16.31.20:8020, Ident: (token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@COSTA85.SG, renewer=yarn, realUser=, issueDate=1481285259349, maxDate=1481890059349, sequenceNumber=2, masterKeyId=2)
16/12/09 21:07:39 INFO input.FileInputFormat: Total input paths to process : 10
16/12/09 21:07:39 INFO mapreduce.JobSubmitter: number of splits:10
16/12/09 21:07:39 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481284833585_0002
16/12/09 21:07:39 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.16.31.20:8020, Ident: (token for orchard: HDFS_DELEGATION_TOKEN owner=orchard@COSTA85.SG, renewer=yarn, realUser=, issueDate=1481285259349, maxDate=1481890059349, sequenceNumber=2, masterKeyId=2)
16/12/09 21:07:40 INFO impl.YarnClientImpl: Submitted application application_1481284833585_0002
16/12/09 21:07:40 INFO mapreduce.Job: The url to track the job: http://clouderaseb00.gitcluster.com:8088/proxy/application_1481284833585_0002/
16/12/09 21:07:40 INFO mapreduce.Job: Running job: job_1481284833585_0002
16/12/09 21:07:48 INFO mapreduce.Job: Job job_1481284833585_0002 running in uber mode : false
16/12/09 21:07:48 INFO mapreduce.Job:  map 0% reduce 0%
16/12/09 21:07:54 INFO mapreduce.Job:  map 20% reduce 0%
16/12/09 21:07:55 INFO mapreduce.Job:  map 30% reduce 0%
16/12/09 21:07:57 INFO mapreduce.Job:  map 60% reduce 0%
16/12/09 21:07:59 INFO mapreduce.Job:  map 100% reduce 0%
16/12/09 21:08:05 INFO mapreduce.Job:  map 100% reduce 100%
16/12/09 21:08:05 INFO mapreduce.Job: Job job_1481284833585_0002 completed successfully
16/12/09 21:08:05 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=98
                FILE: Number of bytes written=1363998
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=2860
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=43
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=10
                Launched reduce tasks=1
                Data-local map tasks=10
                Total time spent by all maps in occupied slots (ms)=68245
                Total time spent by all reduces in occupied slots (ms)=3162
                Total time spent by all map tasks (ms)=68245
                Total time spent by all reduce tasks (ms)=3162
                Total vcore-seconds taken by all map tasks=68245
                Total vcore-seconds taken by all reduce tasks=3162
                Total megabyte-seconds taken by all map tasks=69882880
                Total megabyte-seconds taken by all reduce tasks=3237888
        Map-Reduce Framework
                Map input records=10
                Map output records=20
                Map output bytes=180
                Map output materialized bytes=340
                Input split bytes=1680
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=340
                Reduce input records=20
                Reduce output records=0
                Spilled Records=40
                Shuffled Maps =10
                Failed Shuffles=0
                Merged Map outputs=10
                GC time elapsed (ms)=339
                CPU time spent (ms)=5670
                Physical memory (bytes) snapshot=4727824384
                Virtual memory (bytes) snapshot=17218797568
                Total committed heap usage (bytes)=5517082624
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=1180
        File Output Format Counters
                Bytes Written=97
Job Finished in 26.71 seconds
Estimated value of Pi is 3.14800000000000000000
[orchard@clouderaseb02 ~]$

```