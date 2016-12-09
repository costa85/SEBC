```
[raffles@clouderaseb02 ~]$ kinit raffles
Password for raffles@COSTA85.SG:
[raffles@clouderaseb02 ~]$ ll
total 140
-rw-r--r-- 1 raffles root 142551 Dec  9 20:29 hadoop-examples.jar
[raffles@clouderaseb02 ~]$ time hadoop jar hadoop-examples.jar terasort /user/raffles/tgen512m /user/raffles/tgen512m/output
16/12/09 21:03:14 INFO terasort.TeraSort: starting
16/12/09 21:03:15 INFO hdfs.DFSClient: Created token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@COSTA85.SG, renewer=yarn, realUser=, issueDate=1481284995799, maxDate=1481889795799, sequenceNumber=1, masterKeyId=2 on 172.16.31.20:8020
16/12/09 21:03:15 INFO security.TokenCache: Got dt for hdfs://clouderaseb00.gitcluster.com:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.16.31.20:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@COSTA85.SG, renewer=yarn, realUser=, issueDate=1481284995799, maxDate=1481889795799, sequenceNumber=1, masterKeyId=2)
16/12/09 21:03:15 INFO input.FileInputFormat: Total input paths to process : 8
Spent 378ms computing base-splits.
Spent 3ms computing TeraScheduler splits.
Computing input splits took 382ms
Sampling 10 splits of 80
Making 6 from 100000 sampled records
Computing parititions took 547ms
Spent 932ms computing partitions.
16/12/09 21:03:16 INFO client.RMProxy: Connecting to ResourceManager at clouderaseb00.gitcluster.com/172.16.31.20:8032
16/12/09 21:03:17 INFO mapreduce.JobSubmitter: number of splits:80
16/12/09 21:03:17 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481284833585_0001
16/12/09 21:03:17 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.16.31.20:8020, Ident: (token for raffles: HDFS_DELEGATION_TOKEN owner=raffles@COSTA85.SG, renewer=yarn, realUser=, issueDate=1481284995799, maxDate=1481889795799, sequenceNumber=1, masterKeyId=2)
16/12/09 21:03:18 INFO impl.YarnClientImpl: Submitted application application_1481284833585_0001
16/12/09 21:03:18 INFO mapreduce.Job: The url to track the job: http://clouderaseb00.gitcluster.com:8088/proxy/application_1481284833585_0001/
16/12/09 21:03:18 INFO mapreduce.Job: Running job: job_1481284833585_0001
16/12/09 21:03:27 INFO mapreduce.Job: Job job_1481284833585_0001 running in uber mode : false
16/12/09 21:03:27 INFO mapreduce.Job:  map 0% reduce 0%
16/12/09 21:03:35 INFO mapreduce.Job:  map 3% reduce 0%
16/12/09 21:03:36 INFO mapreduce.Job:  map 4% reduce 0%
16/12/09 21:03:42 INFO mapreduce.Job:  map 14% reduce 0%
16/12/09 21:03:43 INFO mapreduce.Job:  map 17% reduce 0%
16/12/09 21:03:50 INFO mapreduce.Job:  map 22% reduce 0%
16/12/09 21:03:51 INFO mapreduce.Job:  map 28% reduce 0%
16/12/09 21:03:52 INFO mapreduce.Job:  map 31% reduce 0%
16/12/09 21:03:57 INFO mapreduce.Job:  map 34% reduce 0%
16/12/09 21:03:58 INFO mapreduce.Job:  map 35% reduce 0%
16/12/09 21:04:00 INFO mapreduce.Job:  map 39% reduce 0%
16/12/09 21:04:01 INFO mapreduce.Job:  map 45% reduce 0%
16/12/09 21:04:04 INFO mapreduce.Job:  map 47% reduce 0%
16/12/09 21:04:05 INFO mapreduce.Job:  map 49% reduce 0%
16/12/09 21:04:08 INFO mapreduce.Job:  map 51% reduce 0%
16/12/09 21:04:09 INFO mapreduce.Job:  map 54% reduce 0%
16/12/09 21:04:10 INFO mapreduce.Job:  map 59% reduce 0%
16/12/09 21:04:11 INFO mapreduce.Job:  map 61% reduce 0%
16/12/09 21:04:12 INFO mapreduce.Job:  map 63% reduce 0%
16/12/09 21:04:17 INFO mapreduce.Job:  map 64% reduce 0%
16/12/09 21:04:18 INFO mapreduce.Job:  map 73% reduce 0%
16/12/09 21:04:19 INFO mapreduce.Job:  map 76% reduce 0%
16/12/09 21:04:24 INFO mapreduce.Job:  map 77% reduce 0%
16/12/09 21:04:25 INFO mapreduce.Job:  map 80% reduce 0%
16/12/09 21:04:26 INFO mapreduce.Job:  map 82% reduce 0%
16/12/09 21:04:27 INFO mapreduce.Job:  map 86% reduce 0%
16/12/09 21:04:28 INFO mapreduce.Job:  map 89% reduce 0%
16/12/09 21:04:29 INFO mapreduce.Job:  map 90% reduce 0%
16/12/09 21:04:31 INFO mapreduce.Job:  map 93% reduce 0%
16/12/09 21:04:32 INFO mapreduce.Job:  map 95% reduce 0%
16/12/09 21:04:35 INFO mapreduce.Job:  map 96% reduce 0%
16/12/09 21:04:36 INFO mapreduce.Job:  map 99% reduce 0%
16/12/09 21:04:38 INFO mapreduce.Job:  map 99% reduce 6%
16/12/09 21:04:39 INFO mapreduce.Job:  map 99% reduce 14%
16/12/09 21:04:40 INFO mapreduce.Job:  map 99% reduce 19%
16/12/09 21:04:41 INFO mapreduce.Job:  map 99% reduce 23%
16/12/09 21:04:42 INFO mapreduce.Job:  map 100% reduce 24%
16/12/09 21:04:43 INFO mapreduce.Job:  map 100% reduce 25%
16/12/09 21:04:44 INFO mapreduce.Job:  map 100% reduce 31%
16/12/09 21:04:45 INFO mapreduce.Job:  map 100% reduce 36%
16/12/09 21:04:46 INFO mapreduce.Job:  map 100% reduce 44%
16/12/09 21:04:47 INFO mapreduce.Job:  map 100% reduce 56%
16/12/09 21:04:48 INFO mapreduce.Job:  map 100% reduce 58%
16/12/09 21:04:49 INFO mapreduce.Job:  map 100% reduce 65%
16/12/09 21:04:50 INFO mapreduce.Job:  map 100% reduce 71%
16/12/09 21:04:52 INFO mapreduce.Job:  map 100% reduce 72%
16/12/09 21:04:53 INFO mapreduce.Job:  map 100% reduce 75%
16/12/09 21:04:54 INFO mapreduce.Job:  map 100% reduce 82%
16/12/09 21:04:56 INFO mapreduce.Job:  map 100% reduce 84%
16/12/09 21:04:57 INFO mapreduce.Job:  map 100% reduce 86%
16/12/09 21:05:10 INFO mapreduce.Job:  map 100% reduce 88%
16/12/09 21:05:14 INFO mapreduce.Job:  map 100% reduce 90%
16/12/09 21:05:15 INFO mapreduce.Job:  map 100% reduce 91%
16/12/09 21:05:17 INFO mapreduce.Job:  map 100% reduce 93%
16/12/09 21:05:18 INFO mapreduce.Job:  map 100% reduce 95%
16/12/09 21:05:20 INFO mapreduce.Job:  map 100% reduce 96%
16/12/09 21:05:26 INFO mapreduce.Job:  map 100% reduce 98%
16/12/09 21:05:27 INFO mapreduce.Job:  map 100% reduce 99%
16/12/09 21:05:30 INFO mapreduce.Job:  map 100% reduce 100%
16/12/09 21:05:30 INFO mapreduce.Job: Job job_1481284833585_0001 completed successfully
16/12/09 21:05:30 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=2291348381
                FILE: Number of bytes written=4546757013
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5120011200
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=258
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=80
                Launched reduce tasks=6
                Data-local map tasks=80
                Total time spent by all maps in occupied slots (ms)=627495
                Total time spent by all reduces in occupied slots (ms)=299343
                Total time spent by all map tasks (ms)=627495
                Total time spent by all reduce tasks (ms)=299343
                Total vcore-seconds taken by all map tasks=627495
                Total vcore-seconds taken by all reduce tasks=299343
                Total megabyte-seconds taken by all map tasks=642554880
                Total megabyte-seconds taken by all reduce tasks=306527232
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Map output bytes=5222400000
                Map output materialized bytes=2244678632
                Input split bytes=11200
                Combine input records=0
                Combine output records=0
                Reduce input groups=51200000
                Reduce shuffle bytes=2244678632
                Reduce input records=51200000
                Reduce output records=51200000
                Spilled Records=102400000
                Shuffled Maps =480
                Failed Shuffles=0
                Merged Map outputs=480
                GC time elapsed (ms)=12328
                CPU time spent (ms)=401790
                Physical memory (bytes) snapshot=45235695616
                Virtual memory (bytes) snapshot=134682939392
                Total committed heap usage (bytes)=52461830144
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5120000000
        File Output Format Counters
                Bytes Written=5120000000
16/12/09 21:05:30 INFO terasort.TeraSort: done

real    2m17.029s
user    0m6.857s
sys     0m0.278s
[raffles@clouderaseb02 ~]$

```