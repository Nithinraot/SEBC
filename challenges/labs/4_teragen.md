As user jimenez, use teragen to generate a 65,536,000-record dataset

he full teragen command and output ->

[jimenez@ip-172-31-35-195 jars]$ time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.13.3.jar teragen -D dfs.block.size=67108864 -Dmapreduce.map.memory.mb=512 -Dmapred.map.tasks=8 65536000 /user/jimenez/tgen/
18/05/17 08:48:11 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-38-16.us-east-2.compute.internal/172.31.38.16:8032
18/05/17 08:48:12 INFO terasort.TeraGen: Generating 65536000 using 8
18/05/17 08:48:12 INFO mapreduce.JobSubmitter: number of splits:8
18/05/17 08:48:12 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/05/17 08:48:12 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/05/17 08:48:12 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526545005385_0003
18/05/17 08:48:12 INFO impl.YarnClientImpl: Submitted application application_1526545005385_0003
18/05/17 08:48:12 INFO mapreduce.Job: The url to track the job: http://ip-172-31-38-16.us-east-2.compute.internal:8088/proxy/application_1526545005385_0003/
18/05/17 08:48:12 INFO mapreduce.Job: Running job: job_1526545005385_0003
18/05/17 08:48:19 INFO mapreduce.Job: Job job_1526545005385_0003 running in uber mode : false
18/05/17 08:48:19 INFO mapreduce.Job:  map 0% reduce 0%
18/05/17 08:48:36 INFO mapreduce.Job:  map 25% reduce 0%
18/05/17 08:48:38 INFO mapreduce.Job:  map 38% reduce 0%
18/05/17 08:48:41 INFO mapreduce.Job:  map 42% reduce 0%
18/05/17 08:48:42 INFO mapreduce.Job:  map 48% reduce 0%
18/05/17 08:48:44 INFO mapreduce.Job:  map 51% reduce 0%
18/05/17 08:48:47 INFO mapreduce.Job:  map 53% reduce 0%
18/05/17 08:48:48 INFO mapreduce.Job:  map 56% reduce 0%
18/05/17 08:48:50 INFO mapreduce.Job:  map 58% reduce 0%
18/05/17 08:48:51 INFO mapreduce.Job:  map 59% reduce 0%
18/05/17 08:48:53 INFO mapreduce.Job:  map 61% reduce 0%
18/05/17 08:48:54 INFO mapreduce.Job:  map 63% reduce 0%
18/05/17 08:48:56 INFO mapreduce.Job:  map 70% reduce 0%
18/05/17 08:48:59 INFO mapreduce.Job:  map 72% reduce 0%
18/05/17 08:49:01 INFO mapreduce.Job:  map 73% reduce 0%
18/05/17 08:49:05 INFO mapreduce.Job:  map 74% reduce 0%
18/05/17 08:49:07 INFO mapreduce.Job:  map 78% reduce 0%
18/05/17 08:49:08 INFO mapreduce.Job:  map 79% reduce 0%
18/05/17 08:49:09 INFO mapreduce.Job:  map 85% reduce 0%
18/05/17 08:49:13 INFO mapreduce.Job:  map 93% reduce 0%
18/05/17 08:49:15 INFO mapreduce.Job:  map 100% reduce 0%
18/05/17 08:49:15 INFO mapreduce.Job: Job job_1526545005385_0003 completed successfully
18/05/17 08:49:16 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=1184840
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=682
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=32
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Launched map tasks=8
                Other local map tasks=8
                Total time spent by all maps in occupied slots (ms)=254859
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=254859
                Total vcore-milliseconds taken by all map tasks=254859
                Total megabyte-milliseconds taken by all map tasks=260975616
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=682
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1320
                CPU time spent (ms)=123210
                Physical memory (bytes) snapshot=1992957952
                Virtual memory (bytes) snapshot=18822139904
                Total committed heap usage (bytes)=1862270976
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

* The result of the time command
real    1m7.020s
user    0m8.460s
sys     0m0.444s


*
The command and output of hdfs dfs -ls /user/jimenez/tgen
[jimenez@ip-172-31-35-195 jars]$ hdfs dfs -ls /user/jimenez/tgen
Found 9 items
-rw-r--r--   3 jimenez supergroup          0 2018-05-17 08:49 /user/jimenez/tgen/_SUCCESS
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 08:48 /user/jimenez/tgen/part-m-00000
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 08:48 /user/jimenez/tgen/part-m-00001
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 08:48 /user/jimenez/tgen/part-m-00002
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 08:49 /user/jimenez/tgen/part-m-00003
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 08:48 /user/jimenez/tgen/part-m-00004
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 08:49 /user/jimenez/tgen/part-m-00005
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 08:49 /user/jimenez/tgen/part-m-00006
-rw-r--r--   3 jimenez supergroup  819200000 2018-05-17 08:49 /user/jimenez/tgen/part-m-00007


*The command and output of hadoop fsck -blocks /user/jimenez
[jimenez@ip-172-31-35-195 jars]$ hadoop fsck -blocks /user/jimenez
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-35-195.us-east-2.compute.internal:50070/fsck?ugi=jimenez&blocks=1&path=%2Fuser%2Fjimenez
FSCK started by jimenez (auth:SIMPLE) from /172.31.35.195 for path /user/jimenez at Thu May 17 08:50:43 UTC 2018
..................Status: HEALTHY
 Total size:    13107200000 B
 Total dirs:    8
 Total files:   18
 Total symlinks:                0
 Total blocks (validated):      208 (avg. block size 63015384 B)
 Minimally replicated blocks:   208 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Thu May 17 08:50:43 UTC 2018 in 7 milliseconds


The filesystem under path '/user/jimenez' is HEALTHY





