## <center> Teragen testing & HDFS

* The full teragen command and output

[groot@ip-172-31-24-103 jars]$ time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.11.2.jar teragen -D dfs.block.size=67108864 -Dmapreduce.job.maps=40 -Dmapreduce.map.memory.mb=1024 -Dmapred.map.tasks=40 50000000 /user/groot/tgen/
18/05/18 04:51:17 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-20-193.us-east-2.compute.internal/172.31.20.193:8032
18/05/18 04:51:17 INFO terasort.TeraGen: Generating 50000000 using 40
18/05/18 04:51:17 INFO mapreduce.JobSubmitter: number of splits:40
18/05/18 04:51:17 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/05/18 04:51:17 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
18/05/18 04:51:18 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526618136466_0003
18/05/18 04:51:18 INFO impl.YarnClientImpl: Submitted application application_1526618136466_0003
18/05/18 04:51:18 INFO mapreduce.Job: The url to track the job: http://ip-172-31-20-193.us-east-2.compute.internal:8088/proxy/application_1526618136466_0003/
18/05/18 04:51:18 INFO mapreduce.Job: Running job: job_1526618136466_0003
18/05/18 04:51:24 INFO mapreduce.Job: Job job_1526618136466_0003 running in uber mode : false
18/05/18 04:51:24 INFO mapreduce.Job:  map 0% reduce 0%
18/05/18 04:51:31 INFO mapreduce.Job:  map 3% reduce 0%
18/05/18 04:51:32 INFO mapreduce.Job:  map 13% reduce 0%
18/05/18 04:51:33 INFO mapreduce.Job:  map 17% reduce 0%
18/05/18 04:51:37 INFO mapreduce.Job:  map 20% reduce 0%
18/05/18 04:51:38 INFO mapreduce.Job:  map 22% reduce 0%
18/05/18 04:51:39 INFO mapreduce.Job:  map 30% reduce 0%
18/05/18 04:51:40 INFO mapreduce.Job:  map 32% reduce 0%
18/05/18 04:51:41 INFO mapreduce.Job:  map 35% reduce 0%
18/05/18 04:51:43 INFO mapreduce.Job:  map 38% reduce 0%
18/05/18 04:51:45 INFO mapreduce.Job:  map 47% reduce 0%
18/05/18 04:51:47 INFO mapreduce.Job:  map 50% reduce 0%
18/05/18 04:51:50 INFO mapreduce.Job:  map 52% reduce 0%
18/05/18 04:51:52 INFO mapreduce.Job:  map 55% reduce 0%
18/05/18 04:51:55 INFO mapreduce.Job:  map 63% reduce 0%
18/05/18 04:51:57 INFO mapreduce.Job:  map 65% reduce 0%
18/05/18 04:52:00 INFO mapreduce.Job:  map 70% reduce 0%
18/05/18 04:52:01 INFO mapreduce.Job:  map 73% reduce 0%
18/05/18 04:52:02 INFO mapreduce.Job:  map 75% reduce 0%
18/05/18 04:52:05 INFO mapreduce.Job:  map 77% reduce 0%
18/05/18 04:52:06 INFO mapreduce.Job:  map 82% reduce 0%
18/05/18 04:52:07 INFO mapreduce.Job:  map 85% reduce 0%
18/05/18 04:52:11 INFO mapreduce.Job:  map 88% reduce 0%
18/05/18 04:52:12 INFO mapreduce.Job:  map 95% reduce 0%
18/05/18 04:52:15 INFO mapreduce.Job:  map 100% reduce 0%
18/05/18 04:52:15 INFO mapreduce.Job: Job job_1526618136466_0003 completed successfully
18/05/18 04:52:15 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=5117670
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=3423
                HDFS: Number of bytes written=5000000000
                HDFS: Number of read operations=160
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=80
        Job Counters
                Launched map tasks=40
                Other local map tasks=40
                Total time spent by all maps in occupied slots (ms)=281646
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=281646
                Total vcore-milliseconds taken by all map tasks=281646
                Total megabyte-milliseconds taken by all map tasks=288405504
        Map-Reduce Framework
                Map input records=50000000
                Map output records=50000000
                Input split bytes=3423
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=4429
                CPU time spent (ms)=147690
                Physical memory (bytes) snapshot=11771588608
                Virtual memory (bytes) snapshot=111583490048
                Total committed heap usage (bytes)=12838240256
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=107387891658806101
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=5000000000

real    1m0.180s
user    0m7.222s
sys     0m0.486s



The result of the time command
The command and output of hdfs dfs -ls /user/groot/tgen
^C[groot@ip-172-31-24-103 jars]$ hdfs dfs -ls /user/groot/tgen
Found 41 items
-rw-r--r--   3 groot supergroup          0 2018-05-18 04:52 /user/groot/tgen/_SUCCESS
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00000
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00001
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00002
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00003
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00004
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00005
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00006
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00007
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00008
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00009
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00010
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00011
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00012
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00013
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00014
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00015
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00016
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00017
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00018
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00019
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00020
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00021
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00022
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00023
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00024
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00025
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00026
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00027
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:51 /user/groot/tgen/part-m-00028
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00029
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00030
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00031
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00032
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00033
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00034
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00035
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00036
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00037
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00038
-rw-r--r--   3 groot supergroup  125000000 2018-05-18 04:52 /user/groot/tgen/part-m-00039


The command and output of hadoop fsck -blocks /user/groot

[groot@ip-172-31-24-103 jars]$ hadoop fsck -blocks /user/groot
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-20-193.us-east-2.compute.internal:50070
FSCK started by groot (auth:SIMPLE) from /172.31.24.103 for path /user/groot at Fri May 18 04:56:31 UTC 2018
...................................................Status: HEALTHY
 Total size:    15000000000 B
 Total dirs:    12
 Total files:   51
 Total symlinks:                0
 Total blocks (validated):      232 (avg. block size 64655172 B)
 Minimally replicated blocks:   232 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          4
 Number of racks:               1
FSCK ended at Fri May 18 04:56:31 UTC 2018 in 8 milliseconds


The filesystem under path '/user/groot' is HEALTHY
