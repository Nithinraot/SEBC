## <center> Terasort testing output
time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.11.2.jar terasort /user/groot/tgen /user/groot/tsort

[groot@ip-172-31-25-114 jars]$ time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.11.2.jar terasort /user/groot/tgen /user/groot/tsort
18/05/18 05:41:53 INFO terasort.TeraSort: starting
18/05/18 05:41:54 INFO hdfs.DFSClient: Created token for groot: HDFS_DELEGATION_TOKEN owner=groot/user@NITHINRAOT.SG, renewer=yarn, realUser=, issueDate=1526622114590, maxDate=1527226914590, sequenceNumber=1, masterKeyId=2 on 172.31.20.193:8020
18/05/18 05:41:54 INFO security.TokenCache: Got dt for hdfs://ip-172-31-20-193.us-east-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.20.193:8020, Ident: (token for groot: HDFS_DELEGATION_TOKEN owner=groot/user@NITHINRAOT.SG, renewer=yarn, realUser=, issueDate=1526622114590, maxDate=1527226914590, sequenceNumber=1, masterKeyId=2)
18/05/18 05:41:54 INFO input.FileInputFormat: Total input paths to process : 40
Spent 344ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 348ms
Sampling 10 splits of 80
Making 8 from 100000 sampled records
Computing parititions took 627ms
Spent 978ms computing partitions.
18/05/18 05:41:55 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-20-193.us-east-2.compute.internal/172.31.20.193:8032
18/05/18 05:41:55 INFO mapreduce.JobSubmitter: number of splits:80
18/05/18 05:41:55 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526621995180_0001
18/05/18 05:41:55 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.20.193:8020, Ident: (token for groot: HDFS_DELEGATION_TOKEN owner=groot/user@NITHINRAOT.SG, renewer=yarn, realUser=, issueDate=1526622114590, maxDate=1527226914590, sequenceNumber=1, masterKeyId=2)
18/05/18 05:41:57 INFO impl.YarnClientImpl: Submitted application application_1526621995180_0001
18/05/18 05:41:57 INFO mapreduce.Job: The url to track the job: http://ip-172-31-20-193.us-east-2.compute.internal:8088/proxy/application_1526621995180_0001/
18/05/18 05:41:57 INFO mapreduce.Job: Running job: job_1526621995180_0001
18/05/18 05:42:06 INFO mapreduce.Job: Job job_1526621995180_0001 running in uber mode : false
18/05/18 05:42:06 INFO mapreduce.Job:  map 0% reduce 0%
18/05/18 05:42:14 INFO mapreduce.Job:  map 1% reduce 0%
18/05/18 05:42:19 INFO mapreduce.Job:  map 6% reduce 0%
18/05/18 05:42:20 INFO mapreduce.Job:  map 9% reduce 0%
18/05/18 05:42:21 INFO mapreduce.Job:  map 10% reduce 0%
18/05/18 05:42:26 INFO mapreduce.Job:  map 14% reduce 0%
18/05/18 05:42:27 INFO mapreduce.Job:  map 16% reduce 0%
18/05/18 05:42:30 INFO mapreduce.Job:  map 19% reduce 0%
18/05/18 05:42:32 INFO mapreduce.Job:  map 20% reduce 0%
18/05/18 05:42:33 INFO mapreduce.Job:  map 22% reduce 0%
18/05/18 05:42:34 INFO mapreduce.Job:  map 24% reduce 0%
18/05/18 05:42:35 INFO mapreduce.Job:  map 25% reduce 0%
18/05/18 05:42:38 INFO mapreduce.Job:  map 26% reduce 0%
18/05/18 05:42:39 INFO mapreduce.Job:  map 29% reduce 0%
18/05/18 05:42:41 INFO mapreduce.Job:  map 31% reduce 0%
18/05/18 05:42:42 INFO mapreduce.Job:  map 34% reduce 0%
18/05/18 05:42:44 INFO mapreduce.Job:  map 35% reduce 0%
18/05/18 05:42:47 INFO mapreduce.Job:  map 36% reduce 0%
18/05/18 05:42:48 INFO mapreduce.Job:  map 40% reduce 0%
18/05/18 05:42:49 INFO mapreduce.Job:  map 43% reduce 0%
18/05/18 05:42:50 INFO mapreduce.Job:  map 44% reduce 0%
18/05/18 05:42:55 INFO mapreduce.Job:  map 47% reduce 0%
18/05/18 05:42:56 INFO mapreduce.Job:  map 52% reduce 0%
18/05/18 05:43:01 INFO mapreduce.Job:  map 54% reduce 0%
18/05/18 05:43:02 INFO mapreduce.Job:  map 56% reduce 0%
18/05/18 05:43:03 INFO mapreduce.Job:  map 60% reduce 0%
18/05/18 05:43:04 INFO mapreduce.Job:  map 61% reduce 0%
18/05/18 05:43:07 INFO mapreduce.Job:  map 63% reduce 0%
18/05/18 05:43:09 INFO mapreduce.Job:  map 65% reduce 0%
18/05/18 05:43:10 INFO mapreduce.Job:  map 68% reduce 0%
18/05/18 05:43:11 INFO mapreduce.Job:  map 69% reduce 0%
18/05/18 05:43:12 INFO mapreduce.Job:  map 70% reduce 0%
18/05/18 05:43:13 INFO mapreduce.Job:  map 71% reduce 0%
18/05/18 05:43:16 INFO mapreduce.Job:  map 74% reduce 0%
18/05/18 05:43:17 INFO mapreduce.Job:  map 75% reduce 0%
18/05/18 05:43:18 INFO mapreduce.Job:  map 76% reduce 0%
18/05/18 05:43:19 INFO mapreduce.Job:  map 79% reduce 0%
18/05/18 05:43:20 INFO mapreduce.Job:  map 80% reduce 0%
18/05/18 05:43:23 INFO mapreduce.Job:  map 82% reduce 0%
18/05/18 05:43:24 INFO mapreduce.Job:  map 84% reduce 0%
18/05/18 05:43:25 INFO mapreduce.Job:  map 86% reduce 0%
18/05/18 05:43:27 INFO mapreduce.Job:  map 88% reduce 0%
18/05/18 05:43:28 INFO mapreduce.Job:  map 89% reduce 0%
18/05/18 05:43:30 INFO mapreduce.Job:  map 91% reduce 0%
18/05/18 05:43:31 INFO mapreduce.Job:  map 93% reduce 0%
18/05/18 05:43:35 INFO mapreduce.Job:  map 94% reduce 0%
18/05/18 05:43:37 INFO mapreduce.Job:  map 95% reduce 0%
18/05/18 05:43:40 INFO mapreduce.Job:  map 95% reduce 4%
18/05/18 05:43:41 INFO mapreduce.Job:  map 95% reduce 8%
18/05/18 05:43:42 INFO mapreduce.Job:  map 96% reduce 8%
18/05/18 05:43:43 INFO mapreduce.Job:  map 98% reduce 8%
18/05/18 05:43:46 INFO mapreduce.Job:  map 98% reduce 12%
18/05/18 05:43:47 INFO mapreduce.Job:  map 98% reduce 20%
18/05/18 05:43:49 INFO mapreduce.Job:  map 99% reduce 20%
18/05/18 05:43:53 INFO mapreduce.Job:  map 99% reduce 21%
18/05/18 05:43:59 INFO mapreduce.Job:  map 99% reduce 25%
18/05/18 05:44:04 INFO mapreduce.Job:  map 99% reduce 29%
18/05/18 05:44:27 INFO mapreduce.Job:  map 99% reduce 25%
18/05/18 05:44:33 INFO mapreduce.Job:  map 100% reduce 25%
18/05/18 05:44:34 INFO mapreduce.Job:  map 100% reduce 28%
18/05/18 05:44:35 INFO mapreduce.Job:  map 100% reduce 39%
18/05/18 05:44:36 INFO mapreduce.Job:  map 100% reduce 43%
18/05/18 05:44:40 INFO mapreduce.Job:  map 100% reduce 51%
18/05/18 05:44:41 INFO mapreduce.Job:  map 100% reduce 61%
18/05/18 05:44:42 INFO mapreduce.Job:  map 100% reduce 64%
18/05/18 05:44:44 INFO mapreduce.Job:  map 100% reduce 66%
18/05/18 05:44:45 INFO mapreduce.Job:  map 100% reduce 75%
18/05/18 05:45:00 INFO mapreduce.Job:  map 100% reduce 99%
18/05/18 05:45:02 INFO mapreduce.Job:  map 100% reduce 100%
18/05/18 05:45:04 INFO mapreduce.Job: Job job_1526621995180_0001 completed successfully
18/05/18 05:45:04 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2223163753
                FILE: Number of bytes written=4409783963
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=5000011920
                HDFS: Number of bytes written=5000000000
                HDFS: Number of read operations=264
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=16
        Job Counters
                Killed reduce tasks=1
                Launched map tasks=80
                Launched reduce tasks=9
                Data-local map tasks=80
                Total time spent by all maps in occupied slots (ms)=512670
                Total time spent by all reduces in occupied slots (ms)=504526
                Total time spent by all map tasks (ms)=512670
                Total time spent by all reduce tasks (ms)=504526
                Total vcore-milliseconds taken by all map tasks=512670
                Total vcore-milliseconds taken by all reduce tasks=504526
                Total megabyte-milliseconds taken by all map tasks=524974080
                Total megabyte-milliseconds taken by all reduce tasks=516634624
        Map-Reduce Framework
                Map input records=50000000
                Map output records=50000000
                Map output bytes=5100000000
                Map output materialized bytes=2175163620
                Input split bytes=11920
                Combine input records=0
                Combine output records=0
                Reduce input groups=50000000
                Reduce shuffle bytes=2175163620
                Reduce input records=50000000
                Reduce output records=50000000
                Spilled Records=100000000
                Shuffled Maps =640
                Failed Shuffles=0
                Merged Map outputs=640
                GC time elapsed (ms)=13541
                CPU time spent (ms)=560880
                Physical memory (bytes) snapshot=48229998592
                Virtual memory (bytes) snapshot=246011957248
                Total committed heap usage (bytes)=49601314816
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=5000000000
        File Output Format Counters
                Bytes Written=5000000000
18/05/18 05:45:04 INFO terasort.TeraSort: done

real    3m12.040s
user    0m9.280s
sys     0m0.519s


