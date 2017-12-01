```
[root@ip-172-31-5-226 ec2-user]# su saturn
[saturn@ip-172-31-5-226 ec2-user]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=512 -Dmapred.map.tasks.speculative.execution=false 65536000 /user/saturn/tgen/terasort-input
17/12/01 18:17:01 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-57-117.ec2.internal/172.31.57.117:8032
17/12/01 18:17:02 INFO terasort.TeraSort: Generating 65536000 using 512
17/12/01 18:17:02 INFO mapreduce.JobSubmitter: number of splits:512
17/12/01 18:17:02 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/12/01 18:17:02 INFO Configuration.deprecation: mapred.map.tasks.speculative.execution is deprecated. Instead, use mapreduce.map.speculative
17/12/01 18:17:02 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1512149637212_0002
17/12/01 18:17:02 INFO impl.YarnClientImpl: Submitted application application_1512149637212_0002
17/12/01 18:17:02 INFO mapreduce.Job: The url to track the job: http://ip-172-31-57-117.ec2.internal:8088/proxy/application_1512149637212_0002/
17/12/01 18:17:02 INFO mapreduce.Job: Running job: job_1512149637212_0002
17/12/01 18:17:09 INFO mapreduce.Job: Job job_1512149637212_0002 running in uber mode : false
17/12/01 18:17:09 INFO mapreduce.Job:  map 0% reduce 0%
17/12/01 18:17:18 INFO mapreduce.Job:  map 1% reduce 0%
17/12/01 18:17:20 INFO mapreduce.Job:  map 2% reduce 0%
17/12/01 18:17:23 INFO mapreduce.Job:  map 3% reduce 0%
17/12/01 18:17:25 INFO mapreduce.Job:  map 4% reduce 0%
17/12/01 18:17:28 INFO mapreduce.Job:  map 5% reduce 0%
17/12/01 18:17:31 INFO mapreduce.Job:  map 6% reduce 0%
17/12/01 18:17:33 INFO mapreduce.Job:  map 7% reduce 0%
17/12/01 18:17:36 INFO mapreduce.Job:  map 8% reduce 0%
17/12/01 18:17:38 INFO mapreduce.Job:  map 9% reduce 0%
17/12/01 18:17:39 INFO mapreduce.Job:  map 10% reduce 0%
17/12/01 18:17:44 INFO mapreduce.Job:  map 11% reduce 0%
17/12/01 18:17:46 INFO mapreduce.Job:  map 12% reduce 0%
17/12/01 18:17:47 INFO mapreduce.Job:  map 13% reduce 0%
17/12/01 18:17:51 INFO mapreduce.Job:  map 14% reduce 0%
17/12/01 18:17:56 INFO mapreduce.Job:  map 15% reduce 0%
17/12/01 18:17:57 INFO mapreduce.Job:  map 16% reduce 0%
17/12/01 18:17:58 INFO mapreduce.Job:  map 17% reduce 0%
17/12/01 18:18:00 INFO mapreduce.Job:  map 18% reduce 0%
17/12/01 18:18:05 INFO mapreduce.Job:  map 20% reduce 0%
17/12/01 18:18:08 INFO mapreduce.Job:  map 21% reduce 0%
17/12/01 18:18:11 INFO mapreduce.Job:  map 22% reduce 0%
17/12/01 18:18:14 INFO mapreduce.Job:  map 23% reduce 0%
17/12/01 18:18:15 INFO mapreduce.Job:  map 24% reduce 0%
17/12/01 18:18:19 INFO mapreduce.Job:  map 25% reduce 0%
17/12/01 18:18:21 INFO mapreduce.Job:  map 26% reduce 0%
17/12/01 18:18:23 INFO mapreduce.Job:  map 27% reduce 0%
17/12/01 18:18:25 INFO mapreduce.Job:  map 28% reduce 0%
17/12/01 18:18:29 INFO mapreduce.Job:  map 29% reduce 0%
17/12/01 18:18:32 INFO mapreduce.Job:  map 30% reduce 0%
17/12/01 18:18:33 INFO mapreduce.Job:  map 31% reduce 0%
17/12/01 18:18:35 INFO mapreduce.Job:  map 32% reduce 0%
17/12/01 18:18:40 INFO mapreduce.Job:  map 33% reduce 0%
17/12/01 18:18:42 INFO mapreduce.Job:  map 34% reduce 0%
17/12/01 18:18:43 INFO mapreduce.Job:  map 35% reduce 0%
17/12/01 18:18:45 INFO mapreduce.Job:  map 36% reduce 0%
17/12/01 18:18:49 INFO mapreduce.Job:  map 37% reduce 0%
17/12/01 18:18:51 INFO mapreduce.Job:  map 38% reduce 0%
17/12/01 18:18:54 INFO mapreduce.Job:  map 39% reduce 0%
17/12/01 18:18:55 INFO mapreduce.Job:  map 40% reduce 0%
17/12/01 18:19:00 INFO mapreduce.Job:  map 42% reduce 0%
17/12/01 18:19:03 INFO mapreduce.Job:  map 43% reduce 0%
17/12/01 18:19:06 INFO mapreduce.Job:  map 44% reduce 0%
17/12/01 18:19:09 INFO mapreduce.Job:  map 45% reduce 0%
17/12/01 18:19:11 INFO mapreduce.Job:  map 46% reduce 0%
17/12/01 18:19:15 INFO mapreduce.Job:  map 47% reduce 0%
17/12/01 18:19:18 INFO mapreduce.Job:  map 48% reduce 0%
17/12/01 18:19:19 INFO mapreduce.Job:  map 49% reduce 0%
17/12/01 18:19:22 INFO mapreduce.Job:  map 50% reduce 0%
17/12/01 18:19:25 INFO mapreduce.Job:  map 51% reduce 0%
17/12/01 18:19:28 INFO mapreduce.Job:  map 53% reduce 0%
17/12/01 18:19:31 INFO mapreduce.Job:  map 54% reduce 0%
17/12/01 18:19:36 INFO mapreduce.Job:  map 55% reduce 0%
17/12/01 18:19:37 INFO mapreduce.Job:  map 56% reduce 0%
17/12/01 18:19:39 INFO mapreduce.Job:  map 57% reduce 0%
17/12/01 18:19:42 INFO mapreduce.Job:  map 58% reduce 0%
17/12/01 18:19:45 INFO mapreduce.Job:  map 59% reduce 0%
17/12/01 18:19:46 INFO mapreduce.Job:  map 60% reduce 0%
17/12/01 18:19:49 INFO mapreduce.Job:  map 61% reduce 0%
17/12/01 18:19:53 INFO mapreduce.Job:  map 62% reduce 0%
17/12/01 18:19:54 INFO mapreduce.Job:  map 63% reduce 0%
17/12/01 18:19:55 INFO mapreduce.Job:  map 64% reduce 0%
17/12/01 18:20:00 INFO mapreduce.Job:  map 65% reduce 0%
17/12/01 18:20:04 INFO mapreduce.Job:  map 66% reduce 0%
17/12/01 18:20:05 INFO mapreduce.Job:  map 67% reduce 0%
17/12/01 18:20:08 INFO mapreduce.Job:  map 68% reduce 0%
17/12/01 18:20:10 INFO mapreduce.Job:  map 69% reduce 0%
17/12/01 18:20:12 INFO mapreduce.Job:  map 70% reduce 0%
17/12/01 18:20:13 INFO mapreduce.Job:  map 71% reduce 0%
17/12/01 18:20:19 INFO mapreduce.Job:  map 72% reduce 0%
17/12/01 18:20:20 INFO mapreduce.Job:  map 73% reduce 0%
17/12/01 18:20:21 INFO mapreduce.Job:  map 74% reduce 0%
17/12/01 18:20:25 INFO mapreduce.Job:  map 75% reduce 0%
17/12/01 18:20:27 INFO mapreduce.Job:  map 76% reduce 0%
17/12/01 18:20:30 INFO mapreduce.Job:  map 77% reduce 0%
17/12/01 18:20:32 INFO mapreduce.Job:  map 78% reduce 0%
17/12/01 18:20:34 INFO mapreduce.Job:  map 79% reduce 0%
17/12/01 18:20:37 INFO mapreduce.Job:  map 80% reduce 0%
17/12/01 18:20:39 INFO mapreduce.Job:  map 81% reduce 0%
17/12/01 18:20:42 INFO mapreduce.Job:  map 82% reduce 0%
17/12/01 18:20:46 INFO mapreduce.Job:  map 83% reduce 0%
17/12/01 18:20:47 INFO mapreduce.Job:  map 84% reduce 0%
17/12/01 18:20:49 INFO mapreduce.Job:  map 85% reduce 0%
17/12/01 18:20:53 INFO mapreduce.Job:  map 86% reduce 0%
17/12/01 18:20:55 INFO mapreduce.Job:  map 87% reduce 0%
17/12/01 18:20:57 INFO mapreduce.Job:  map 88% reduce 0%
17/12/01 18:20:59 INFO mapreduce.Job:  map 89% reduce 0%
17/12/01 18:21:03 INFO mapreduce.Job:  map 90% reduce 0%
17/12/01 18:21:05 INFO mapreduce.Job:  map 91% reduce 0%
17/12/01 18:21:06 INFO mapreduce.Job:  map 92% reduce 0%
17/12/01 18:21:10 INFO mapreduce.Job:  map 93% reduce 0%
17/12/01 18:21:12 INFO mapreduce.Job:  map 94% reduce 0%
17/12/01 18:21:14 INFO mapreduce.Job:  map 95% reduce 0%
17/12/01 18:21:16 INFO mapreduce.Job:  map 96% reduce 0%
17/12/01 18:21:19 INFO mapreduce.Job:  map 97% reduce 0%
17/12/01 18:21:21 INFO mapreduce.Job:  map 98% reduce 0%
17/12/01 18:21:24 INFO mapreduce.Job:  map 99% reduce 0%
17/12/01 18:21:25 INFO mapreduce.Job:  map 100% reduce 0%
17/12/01 18:21:29 INFO mapreduce.Job: Job job_1512149637212_0002 completed successfully
17/12/01 18:21:29 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=63197074
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=43897
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=2048
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=1024
        Job Counters
                Launched map tasks=512
                Other local map tasks=512
                Total time spent by all maps in occupied slots (ms)=3888775
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=3888775
                Total vcore-seconds taken by all map tasks=3888775
                Total megabyte-seconds taken by all map tasks=3982105600
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=43897
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=47220
                CPU time spent (ms)=1269490
                Physical memory (bytes) snapshot=128804462592
                Virtual memory (bytes) snapshot=819609710592
                Total committed heap usage (bytes)=262793068544
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

```

```
[saturn@ip-172-31-5-226 ec2-user]$ hdfs dfs -ls /user/saturn/tgen
Found 1 items
drwxr-xr-x   - saturn saturn          0 2017-12-01 18:21 /user/saturn/tgen/terasort-input
```

```
[saturn@ip-172-31-5-226 ec2-user]$ hadoop fsck -blocks /user/saturn
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-57-117.ec2.internal:50070
FSCK started by saturn (auth:SIMPLE) from /172.31.5.226 for path /user/saturn at Fri Dec 01 18:24:07 UTC 2017
....................................................................................................
....................................................................................................
....................................................................................................
....................................................................................................
....................................................................................................
.............Status: HEALTHY
 Total size:    6553600000 B
 Total dirs:    4
 Total files:   513
 Total symlinks:                0
 Total blocks (validated):      512 (avg. block size 12800000 B)
 Minimally replicated blocks:   512 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Fri Dec 01 18:24:07 UTC 2017 in 78 milliseconds


The filesystem under path '/user/saturn' is HEALTHY
```

