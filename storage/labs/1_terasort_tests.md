## Teragen

```
[costa85@clouderaseb02 ~]$ time hadoop jar hadoop-examples.jar teragen \
>     -Ddfs.block.size=33554432 \
>     -Dmapred.map.tasks=4 \
> 100000000 \
>     /user/costa85/input
16/12/06 21:16:13 INFO client.RMProxy: Connecting to ResourceManager at clouderaseb00.gitcluster.com/172.16.31.20:8032
16/12/06 21:16:13 INFO terasort.TeraSort: Generating 100000000 using 4
16/12/06 21:16:13 INFO mapreduce.JobSubmitter: number of splits:4
16/12/06 21:16:13 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
16/12/06 21:16:13 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
16/12/06 21:16:14 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481021947993_0006
16/12/06 21:16:14 INFO impl.YarnClientImpl: Submitted application application_1481021947993_0006
16/12/06 21:16:14 INFO mapreduce.Job: The url to track the job: http://clouderaseb00.gitcluster.com:8088/proxy/application_1481021947993_0006/
16/12/06 21:16:14 INFO mapreduce.Job: Running job: job_1481021947993_0006
16/12/06 21:17:00 INFO mapreduce.Job: Job job_1481021947993_0006 running in uber mode : false
16/12/06 21:17:00 INFO mapreduce.Job:  map 0% reduce 0%
16/12/06 21:17:10 INFO mapreduce.Job:  map 4% reduce 0%
16/12/06 21:17:12 INFO mapreduce.Job:  map 8% reduce 0%
16/12/06 21:17:13 INFO mapreduce.Job:  map 10% reduce 0%
16/12/06 21:17:18 INFO mapreduce.Job:  map 13% reduce 0%
16/12/06 21:17:23 INFO mapreduce.Job:  map 14% reduce 0%
16/12/06 21:17:27 INFO mapreduce.Job:  map 15% reduce 0%
16/12/06 21:17:30 INFO mapreduce.Job:  map 18% reduce 0%
16/12/06 21:17:33 INFO mapreduce.Job:  map 21% reduce 0%
16/12/06 21:17:43 INFO mapreduce.Job:  map 23% reduce 0%
16/12/06 21:17:49 INFO mapreduce.Job:  map 25% reduce 0%
16/12/06 21:17:52 INFO mapreduce.Job:  map 27% reduce 0%
16/12/06 21:17:55 INFO mapreduce.Job:  map 28% reduce 0%
16/12/06 21:18:00 INFO mapreduce.Job:  map 29% reduce 0%
16/12/06 21:18:03 INFO mapreduce.Job:  map 31% reduce 0%
16/12/06 21:18:06 INFO mapreduce.Job:  map 32% reduce 0%
16/12/06 21:18:14 INFO mapreduce.Job:  map 34% reduce 0%
16/12/06 21:18:17 INFO mapreduce.Job:  map 35% reduce 0%
16/12/06 21:18:20 INFO mapreduce.Job:  map 37% reduce 0%
16/12/06 21:18:27 INFO mapreduce.Job:  map 40% reduce 0%
16/12/06 21:18:30 INFO mapreduce.Job:  map 41% reduce 0%
16/12/06 21:18:36 INFO mapreduce.Job:  map 43% reduce 0%
16/12/06 21:18:39 INFO mapreduce.Job:  map 44% reduce 0%
16/12/06 21:18:43 INFO mapreduce.Job:  map 45% reduce 0%
16/12/06 21:18:46 INFO mapreduce.Job:  map 47% reduce 0%
16/12/06 21:18:53 INFO mapreduce.Job:  map 48% reduce 0%
16/12/06 21:18:56 INFO mapreduce.Job:  map 49% reduce 0%
16/12/06 21:19:01 INFO mapreduce.Job:  map 50% reduce 0%
16/12/06 21:19:10 INFO mapreduce.Job:  map 52% reduce 0%
16/12/06 21:19:14 INFO mapreduce.Job:  map 54% reduce 0%
16/12/06 21:19:17 INFO mapreduce.Job:  map 55% reduce 0%
16/12/06 21:19:20 INFO mapreduce.Job:  map 58% reduce 0%
16/12/06 21:19:25 INFO mapreduce.Job:  map 60% reduce 0%
16/12/06 21:19:30 INFO mapreduce.Job:  map 62% reduce 0%
16/12/06 21:19:33 INFO mapreduce.Job:  map 64% reduce 0%
16/12/06 21:19:36 INFO mapreduce.Job:  map 65% reduce 0%
16/12/06 21:19:40 INFO mapreduce.Job:  map 66% reduce 0%
16/12/06 21:19:44 INFO mapreduce.Job:  map 67% reduce 0%
16/12/06 21:19:47 INFO mapreduce.Job:  map 68% reduce 0%
16/12/06 21:19:51 INFO mapreduce.Job:  map 69% reduce 0%
16/12/06 21:19:56 INFO mapreduce.Job:  map 71% reduce 0%
16/12/06 21:19:59 INFO mapreduce.Job:  map 72% reduce 0%
16/12/06 21:20:02 INFO mapreduce.Job:  map 75% reduce 0%
16/12/06 21:20:08 INFO mapreduce.Job:  map 76% reduce 0%
16/12/06 21:20:15 INFO mapreduce.Job:  map 79% reduce 0%
16/12/06 21:20:18 INFO mapreduce.Job:  map 80% reduce 0%
16/12/06 21:20:24 INFO mapreduce.Job:  map 81% reduce 0%
16/12/06 21:20:32 INFO mapreduce.Job:  map 83% reduce 0%
16/12/06 21:20:35 INFO mapreduce.Job:  map 86% reduce 0%
16/12/06 21:20:44 INFO mapreduce.Job:  map 88% reduce 0%
16/12/06 21:20:49 INFO mapreduce.Job:  map 91% reduce 0%
16/12/06 21:20:52 INFO mapreduce.Job:  map 92% reduce 0%
16/12/06 21:20:55 INFO mapreduce.Job:  map 93% reduce 0%
16/12/06 21:20:58 INFO mapreduce.Job:  map 94% reduce 0%
16/12/06 21:21:01 INFO mapreduce.Job:  map 96% reduce 0%
16/12/06 21:21:04 INFO mapreduce.Job:  map 97% reduce 0%
16/12/06 21:21:07 INFO mapreduce.Job:  map 98% reduce 0%
16/12/06 21:21:10 INFO mapreduce.Job:  map 100% reduce 0%
16/12/06 21:21:21 INFO mapreduce.Job: Job job_1481021947993_0006 completed successfully
16/12/06 21:21:26 INFO mapred.ClientServiceDelegate: Application state is completed. FinalApplicationStatus=SUCCEEDED. Redirecting to job history server
16/12/06 21:21:26 INFO mapreduce.Job: Counters: 30
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=494700
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=493955
                Total time spent by all map tasks (ms)=493955
                Total vcore-seconds taken by all map tasks=493955
                Total megabyte-seconds taken by all map tasks=505809920
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1167
                CPU time spent (ms)=126000
                Physical memory (bytes) snapshot=955322368
                Virtual memory (bytes) snapshot=6260408320
                Total committed heap usage (bytes)=592969728
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    5m15.318s
user    0m5.389s
sys     0m0.374s
```

## Terasort

```
[costa85@clouderaseb02 ~]$ time hadoop jar hadoop-examples.jar terasort /user/costa85/input /user/costa85/output   16/12/06 21:25:44 INFO terasort.TeraSort: starting
16/12/06 21:25:45 INFO input.FileInputFormat: Total input paths to process : 4
Spent 297ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 304ms
Sampling 10 splits of 300
Making 6 from 100000 sampled records
Computing parititions took 624ms
Spent 930ms computing partitions.
16/12/06 21:25:46 INFO client.RMProxy: Connecting to ResourceManager at clouderaseb00.gitcluster.com/172.16.31.20:8032
16/12/06 21:25:46 INFO mapreduce.JobSubmitter: number of splits:300
16/12/06 21:25:46 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1481021947993_0007
16/12/06 21:25:47 INFO impl.YarnClientImpl: Submitted application application_1481021947993_0007
16/12/06 21:25:47 INFO mapreduce.Job: The url to track the job: http://clouderaseb00.gitcluster.com:8088/proxy/application_1481021947993_0007/
16/12/06 21:25:47 INFO mapreduce.Job: Running job: job_1481021947993_0007
16/12/06 21:25:52 INFO mapreduce.Job: Job job_1481021947993_0007 running in uber mode : false
16/12/06 21:25:52 INFO mapreduce.Job:  map 0% reduce 0%
16/12/06 21:25:59 INFO mapreduce.Job:  map 1% reduce 0%
16/12/06 21:26:09 INFO mapreduce.Job:  map 2% reduce 0%
16/12/06 21:26:14 INFO mapreduce.Job:  map 3% reduce 0%
16/12/06 21:26:24 INFO mapreduce.Job:  map 4% reduce 0%
16/12/06 21:26:29 INFO mapreduce.Job:  map 5% reduce 0%
16/12/06 21:26:39 INFO mapreduce.Job:  map 6% reduce 0%
16/12/06 21:26:44 INFO mapreduce.Job:  map 7% reduce 0%
16/12/06 21:26:54 INFO mapreduce.Job:  map 8% reduce 0%
16/12/06 21:26:59 INFO mapreduce.Job:  map 9% reduce 0%
16/12/06 21:27:09 INFO mapreduce.Job:  map 10% reduce 0%
16/12/06 21:27:14 INFO mapreduce.Job:  map 11% reduce 0%
16/12/06 21:27:25 INFO mapreduce.Job:  map 12% reduce 0%
16/12/06 21:27:31 INFO mapreduce.Job:  map 13% reduce 0%
16/12/06 21:27:40 INFO mapreduce.Job:  map 14% reduce 0%
16/12/06 21:27:46 INFO mapreduce.Job:  map 15% reduce 0%
16/12/06 21:27:55 INFO mapreduce.Job:  map 16% reduce 0%
16/12/06 21:28:01 INFO mapreduce.Job:  map 17% reduce 0%
16/12/06 21:28:10 INFO mapreduce.Job:  map 18% reduce 0%
16/12/06 21:28:16 INFO mapreduce.Job:  map 19% reduce 0%
16/12/06 21:28:25 INFO mapreduce.Job:  map 20% reduce 0%
16/12/06 21:28:31 INFO mapreduce.Job:  map 21% reduce 0%
16/12/06 21:28:40 INFO mapreduce.Job:  map 22% reduce 0%
16/12/06 21:28:46 INFO mapreduce.Job:  map 23% reduce 0%
16/12/06 21:28:55 INFO mapreduce.Job:  map 24% reduce 0%
16/12/06 21:29:01 INFO mapreduce.Job:  map 25% reduce 0%
16/12/06 21:29:10 INFO mapreduce.Job:  map 26% reduce 0%
16/12/06 21:29:16 INFO mapreduce.Job:  map 27% reduce 0%
16/12/06 21:29:25 INFO mapreduce.Job:  map 28% reduce 0%
16/12/06 21:29:31 INFO mapreduce.Job:  map 29% reduce 0%
16/12/06 21:29:40 INFO mapreduce.Job:  map 30% reduce 0%
16/12/06 21:29:46 INFO mapreduce.Job:  map 31% reduce 0%
16/12/06 21:29:55 INFO mapreduce.Job:  map 32% reduce 0%
16/12/06 21:30:01 INFO mapreduce.Job:  map 33% reduce 0%
16/12/06 21:30:10 INFO mapreduce.Job:  map 34% reduce 0%
16/12/06 21:30:16 INFO mapreduce.Job:  map 35% reduce 0%
16/12/06 21:30:26 INFO mapreduce.Job:  map 36% reduce 0%
16/12/06 21:30:32 INFO mapreduce.Job:  map 37% reduce 0%
16/12/06 21:30:41 INFO mapreduce.Job:  map 38% reduce 0%
16/12/06 21:30:47 INFO mapreduce.Job:  map 39% reduce 0%
16/12/06 21:30:56 INFO mapreduce.Job:  map 40% reduce 0%
16/12/06 21:31:02 INFO mapreduce.Job:  map 41% reduce 0%
16/12/06 21:31:11 INFO mapreduce.Job:  map 42% reduce 0%
16/12/06 21:31:18 INFO mapreduce.Job:  map 43% reduce 0%
16/12/06 21:31:26 INFO mapreduce.Job:  map 44% reduce 0%
16/12/06 21:31:33 INFO mapreduce.Job:  map 45% reduce 0%
16/12/06 21:31:41 INFO mapreduce.Job:  map 46% reduce 0%
16/12/06 21:31:48 INFO mapreduce.Job:  map 47% reduce 0%
16/12/06 21:31:56 INFO mapreduce.Job:  map 48% reduce 0%
16/12/06 21:32:03 INFO mapreduce.Job:  map 49% reduce 0%
16/12/06 21:32:11 INFO mapreduce.Job:  map 50% reduce 0%
16/12/06 21:32:18 INFO mapreduce.Job:  map 51% reduce 0%
16/12/06 21:32:26 INFO mapreduce.Job:  map 52% reduce 0%
16/12/06 21:32:33 INFO mapreduce.Job:  map 53% reduce 0%
16/12/06 21:32:41 INFO mapreduce.Job:  map 54% reduce 0%
16/12/06 21:32:48 INFO mapreduce.Job:  map 55% reduce 0%
16/12/06 21:32:56 INFO mapreduce.Job:  map 56% reduce 0%
16/12/06 21:33:03 INFO mapreduce.Job:  map 57% reduce 0%
16/12/06 21:33:12 INFO mapreduce.Job:  map 58% reduce 0%
16/12/06 21:33:18 INFO mapreduce.Job:  map 59% reduce 0%
16/12/06 21:33:28 INFO mapreduce.Job:  map 60% reduce 0%
16/12/06 21:33:34 INFO mapreduce.Job:  map 61% reduce 0%
16/12/06 21:33:43 INFO mapreduce.Job:  map 62% reduce 0%
16/12/06 21:33:49 INFO mapreduce.Job:  map 63% reduce 0%
16/12/06 21:33:58 INFO mapreduce.Job:  map 64% reduce 0%
16/12/06 21:34:04 INFO mapreduce.Job:  map 65% reduce 0%
16/12/06 21:34:13 INFO mapreduce.Job:  map 66% reduce 0%
16/12/06 21:34:19 INFO mapreduce.Job:  map 67% reduce 0%
16/12/06 21:34:28 INFO mapreduce.Job:  map 68% reduce 0%
16/12/06 21:34:34 INFO mapreduce.Job:  map 69% reduce 0%
16/12/06 21:34:43 INFO mapreduce.Job:  map 70% reduce 0%
16/12/06 21:34:49 INFO mapreduce.Job:  map 71% reduce 0%
16/12/06 21:34:58 INFO mapreduce.Job:  map 72% reduce 0%
16/12/06 21:35:04 INFO mapreduce.Job:  map 73% reduce 0%
16/12/06 21:35:13 INFO mapreduce.Job:  map 74% reduce 0%
16/12/06 21:35:19 INFO mapreduce.Job:  map 75% reduce 0%
16/12/06 21:35:28 INFO mapreduce.Job:  map 76% reduce 0%
16/12/06 21:35:34 INFO mapreduce.Job:  map 77% reduce 0%
16/12/06 21:35:43 INFO mapreduce.Job:  map 78% reduce 0%
16/12/06 21:35:49 INFO mapreduce.Job:  map 79% reduce 0%
16/12/06 21:35:57 INFO mapreduce.Job:  map 80% reduce 0%
16/12/06 21:36:04 INFO mapreduce.Job:  map 81% reduce 0%
16/12/06 21:36:12 INFO mapreduce.Job:  map 81% reduce 3%
16/12/06 21:36:15 INFO mapreduce.Job:  map 81% reduce 4%
16/12/06 21:36:18 INFO mapreduce.Job:  map 81% reduce 5%
16/12/06 21:36:19 INFO mapreduce.Job:  map 82% reduce 5%
16/12/06 21:36:34 INFO mapreduce.Job:  map 83% reduce 5%
16/12/06 21:36:50 INFO mapreduce.Job:  map 84% reduce 5%
16/12/06 21:37:05 INFO mapreduce.Job:  map 85% reduce 5%
16/12/06 21:37:20 INFO mapreduce.Job:  map 86% reduce 5%
16/12/06 21:37:35 INFO mapreduce.Job:  map 87% reduce 5%
16/12/06 21:37:52 INFO mapreduce.Job:  map 88% reduce 5%
16/12/06 21:38:07 INFO mapreduce.Job:  map 89% reduce 5%
16/12/06 21:38:22 INFO mapreduce.Job:  map 90% reduce 5%
16/12/06 21:38:38 INFO mapreduce.Job:  map 91% reduce 5%
16/12/06 21:38:53 INFO mapreduce.Job:  map 92% reduce 5%
16/12/06 21:39:07 INFO mapreduce.Job:  map 93% reduce 5%
16/12/06 21:39:24 INFO mapreduce.Job:  map 94% reduce 5%
16/12/06 21:39:39 INFO mapreduce.Job:  map 95% reduce 5%
16/12/06 21:39:54 INFO mapreduce.Job:  map 96% reduce 5%
16/12/06 21:40:09 INFO mapreduce.Job:  map 97% reduce 5%
16/12/06 21:40:24 INFO mapreduce.Job:  map 98% reduce 5%
16/12/06 21:40:39 INFO mapreduce.Job:  map 99% reduce 5%
16/12/06 21:40:47 INFO mapreduce.Job:  map 99% reduce 6%
16/12/06 21:40:54 INFO mapreduce.Job:  map 100% reduce 6%
16/12/06 21:40:55 INFO mapreduce.Job:  map 100% reduce 0%
16/12/06 21:41:06 INFO mapreduce.Job:  map 100% reduce 3%
16/12/06 21:41:09 INFO mapreduce.Job:  map 100% reduce 7%
16/12/06 21:41:12 INFO mapreduce.Job:  map 100% reduce 8%
16/12/06 21:41:15 INFO mapreduce.Job:  map 100% reduce 10%
16/12/06 21:41:18 INFO mapreduce.Job:  map 100% reduce 15%
16/12/06 21:41:21 INFO mapreduce.Job:  map 100% reduce 23%
16/12/06 21:41:24 INFO mapreduce.Job:  map 100% reduce 25%
16/12/06 21:41:27 INFO mapreduce.Job:  map 100% reduce 27%
16/12/06 21:41:30 INFO mapreduce.Job:  map 100% reduce 28%
16/12/06 21:41:31 INFO mapreduce.Job:  map 100% reduce 29%
16/12/06 21:41:33 INFO mapreduce.Job:  map 100% reduce 31%
16/12/06 21:41:34 INFO mapreduce.Job:  map 100% reduce 32%
16/12/06 21:41:36 INFO mapreduce.Job:  map 100% reduce 33%
16/12/06 21:41:45 INFO mapreduce.Job:  map 100% reduce 36%
16/12/06 21:41:48 INFO mapreduce.Job:  map 100% reduce 40%
16/12/06 21:41:51 INFO mapreduce.Job:  map 100% reduce 41%
16/12/06 21:41:54 INFO mapreduce.Job:  map 100% reduce 43%
16/12/06 21:41:57 INFO mapreduce.Job:  map 100% reduce 44%
16/12/06 21:42:00 INFO mapreduce.Job:  map 100% reduce 56%
16/12/06 21:42:03 INFO mapreduce.Job:  map 100% reduce 58%
16/12/06 21:42:06 INFO mapreduce.Job:  map 100% reduce 61%
16/12/06 21:42:09 INFO mapreduce.Job:  map 100% reduce 63%
16/12/06 21:42:12 INFO mapreduce.Job:  map 100% reduce 65%
16/12/06 21:42:14 INFO mapreduce.Job:  map 100% reduce 66%
16/12/06 21:42:15 INFO mapreduce.Job:  map 100% reduce 67%
16/12/06 21:42:25 INFO mapreduce.Job:  map 100% reduce 68%
16/12/06 21:42:26 INFO mapreduce.Job:  map 100% reduce 70%
16/12/06 21:42:29 INFO mapreduce.Job:  map 100% reduce 71%
16/12/06 21:42:31 INFO mapreduce.Job:  map 100% reduce 72%
16/12/06 21:42:32 INFO mapreduce.Job:  map 100% reduce 74%
16/12/06 21:42:36 INFO mapreduce.Job:  map 100% reduce 75%
16/12/06 21:42:38 INFO mapreduce.Job:  map 100% reduce 76%
16/12/06 21:42:42 INFO mapreduce.Job:  map 100% reduce 78%
16/12/06 21:42:45 INFO mapreduce.Job:  map 100% reduce 83%
16/12/06 21:42:48 INFO mapreduce.Job:  map 100% reduce 85%
16/12/06 21:42:54 INFO mapreduce.Job:  map 100% reduce 87%
16/12/06 21:42:57 INFO mapreduce.Job:  map 100% reduce 88%
16/12/06 21:43:00 INFO mapreduce.Job:  map 100% reduce 89%
16/12/06 21:43:06 INFO mapreduce.Job:  map 100% reduce 91%
16/12/06 21:43:09 INFO mapreduce.Job:  map 100% reduce 95%
16/12/06 21:43:12 INFO mapreduce.Job:  map 100% reduce 96%
16/12/06 21:43:15 INFO mapreduce.Job:  map 100% reduce 97%
16/12/06 21:43:18 INFO mapreduce.Job:  map 100% reduce 98%
16/12/06 21:43:21 INFO mapreduce.Job:  map 100% reduce 99%
16/12/06 21:43:23 INFO mapreduce.Job:  map 100% reduce 100%
16/12/06 21:43:23 INFO mapreduce.Job: Job job_1481021947993_0007 completed successfully
16/12/06 21:43:23 INFO mapreduce.Job: Counters: 51
        File System Counters
                FILE: Number of bytes read=4482346128
                FILE: Number of bytes written=8895804037
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000034800
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=918
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Killed reduce tasks=1
                Launched map tasks=300
                Launched reduce tasks=7
                Data-local map tasks=298
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=1281638
                Total time spent by all reduces in occupied slots (ms)=546893
                Total time spent by all map tasks (ms)=1281638
                Total time spent by all reduce tasks (ms)=546893
                Total vcore-seconds taken by all map tasks=1281638
                Total vcore-seconds taken by all reduce tasks=546893
                Total megabyte-seconds taken by all map tasks=1312397312
                Total megabyte-seconds taken by all reduce tasks=560018432
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375170195
                Input split bytes=34800
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375170195
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =1800
                Failed Shuffles=0
                Merged Map outputs=1800
                GC time elapsed (ms)=19504
                CPU time spent (ms)=1001070
                Physical memory (bytes) snapshot=141216956416
                Virtual memory (bytes) snapshot=480256253952
                Total committed heap usage (bytes)=150779461632
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
16/12/06 21:43:23 INFO terasort.TeraSort: done

real    17m40.417s
user    0m10.246s
sys     0m0.825s
```