```
[raffles@clouderaseb02 ~]$ time hadoop jar hadoop-examples.jar teragen  \
> -Ddfs.block.size=67108864 \
> -Dmapred.map.tasks=8 \
> 51200000 /user/raffles/tgen512m
16/12/09 20:35:39 INFO client.RMProxy: Connecting to ResourceManager at clouderaseb00.gitcluster.com/172.16.31.20:8032
16/12/09 20:35:39 INFO terasort.TeraSort: Generating 51200000 using 8
16/12/09 20:35:39 INFO mapreduce.JobSubmitter: number of splits:8
16/12/09 20:35:39 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
16/12/09 20:35:39 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
16/12/09 20:35:40 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481282140328_0001
16/12/09 20:35:40 INFO impl.YarnClientImpl: Submitted application application_1481282140328_0001
16/12/09 20:35:40 INFO mapreduce.Job: The url to track the job: http://clouderaseb00.gitcluster.com:8088/proxy/application_1481282140328_0001/
16/12/09 20:35:40 INFO mapreduce.Job: Running job: job_1481282140328_0001
16/12/09 20:35:47 INFO mapreduce.Job: Job job_1481282140328_0001 running in uber mode : false
16/12/09 20:35:47 INFO mapreduce.Job:  map 0% reduce 0%
16/12/09 20:35:59 INFO mapreduce.Job:  map 8% reduce 0%
16/12/09 20:36:02 INFO mapreduce.Job:  map 23% reduce 0%
16/12/09 20:36:05 INFO mapreduce.Job:  map 32% reduce 0%
16/12/09 20:36:08 INFO mapreduce.Job:  map 40% reduce 0%
16/12/09 20:36:11 INFO mapreduce.Job:  map 45% reduce 0%
16/12/09 20:36:14 INFO mapreduce.Job:  map 47% reduce 0%
16/12/09 20:36:18 INFO mapreduce.Job:  map 56% reduce 0%
16/12/09 20:36:21 INFO mapreduce.Job:  map 59% reduce 0%
16/12/09 20:36:36 INFO mapreduce.Job:  map 60% reduce 0%
16/12/09 20:36:39 INFO mapreduce.Job:  map 66% reduce 0%
16/12/09 20:36:42 INFO mapreduce.Job:  map 72% reduce 0%
16/12/09 20:36:51 INFO mapreduce.Job:  map 74% reduce 0%
16/12/09 20:36:54 INFO mapreduce.Job:  map 78% reduce 0%
16/12/09 20:36:57 INFO mapreduce.Job:  map 81% reduce 0%
16/12/09 20:37:00 INFO mapreduce.Job:  map 84% reduce 0%
16/12/09 20:37:03 INFO mapreduce.Job:  map 86% reduce 0%
16/12/09 20:37:11 INFO mapreduce.Job:  map 87% reduce 0%
16/12/09 20:37:12 INFO mapreduce.Job:  map 88% reduce 0%
16/12/09 20:37:13 INFO mapreduce.Job:  map 92% reduce 0%
16/12/09 20:37:16 INFO mapreduce.Job:  map 93% reduce 0%
16/12/09 20:37:18 INFO mapreduce.Job:  map 96% reduce 0%
16/12/09 20:37:21 INFO mapreduce.Job:  map 98% reduce 0%
16/12/09 20:37:27 INFO mapreduce.Job:  map 100% reduce 0%
16/12/09 20:37:28 INFO mapreduce.Job: Job job_1481282140328_0001 completed successfully
16/12/09 20:37:28 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=980304
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=682
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=32
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=8
                Other local map tasks=8
                Total time spent by all maps in occupied slots (ms)=665291
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=665291
                Total vcore-seconds taken by all map tasks=665291
                Total megabyte-seconds taken by all map tasks=681257984
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Input split bytes=682
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1053
                CPU time spent (ms)=85570
                Physical memory (bytes) snapshot=2816745472
                Virtual memory (bytes) snapshot=12544241664
                Total committed heap usage (bytes)=3061317632
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=109963291816450258
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=5120000000

real    1m51.754s
user    0m5.230s
sys     0m0.285s
[raffles@clouderaseb02 ~]$ hdfs dfs -ls /user/raffles/tgen512mhdfs dfs -ls /user/raffles/tgen512m
ls: `/user/raffles/tgen512mhdfs': No such file or directory
ls: `dfs': No such file or directory
ls: `-ls': No such file or directory
Found 9 items
-rw-r--r--   3 raffles raffles          0 2016-12-09 20:37 /user/raffles/tgen512m/_SUCCESS
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 20:37 /user/raffles/tgen512m/part-m-00000
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 20:37 /user/raffles/tgen512m/part-m-00001
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 20:37 /user/raffles/tgen512m/part-m-00002
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 20:37 /user/raffles/tgen512m/part-m-00003
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 20:37 /user/raffles/tgen512m/part-m-00004
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 20:37 /user/raffles/tgen512m/part-m-00005
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 20:37 /user/raffles/tgen512m/part-m-00006
-rw-r--r--   3 raffles raffles  640000000 2016-12-09 20:36 /user/raffles/tgen512m/part-m-00007
[raffles@clouderaseb02 ~]$
```