## <center> PI output

[root@ip-172-31-25-114 krb5kdc]# kinit thanos/user@NITHINRAOT.SG
Password for thanos/user@NITHINRAOT.SG:
[root@ip-172-31-25-114 krb5kdc]# cd /opt/cloudera/parcels/CDH-5.11.2-1.cdh5.11.2.p0.4/jars/
[root@ip-172-31-25-114 jars]# time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.11.2.jar pi 2 4
Number of Maps  = 2
Samples per Map = 4
Wrote input for Map #0
Wrote input for Map #1
Starting Job
18/05/18 05:44:24 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-20-193.us-east-2.compute.internal/172.31.20.193:8032
18/05/18 05:44:24 INFO hdfs.DFSClient: Created token for thanos: HDFS_DELEGATION_TOKEN owner=thanos/user@NITHINRAOT.SG, renewer=yarn, realUser=, issueDate=1526622264270, maxDate=1527227064270, sequenceNumber=2, masterKeyId=2 on 172.31.20.193:8020
18/05/18 05:44:24 INFO security.TokenCache: Got dt for hdfs://ip-172-31-20-193.us-east-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.20.193:8020, Ident: (token for thanos: HDFS_DELEGATION_TOKEN owner=thanos/user@NITHINRAOT.SG, renewer=yarn, realUser=, issueDate=1526622264270, maxDate=1527227064270, sequenceNumber=2, masterKeyId=2)
18/05/18 05:44:24 INFO input.FileInputFormat: Total input paths to process : 2
18/05/18 05:44:24 INFO mapreduce.JobSubmitter: number of splits:2
18/05/18 05:44:24 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526621995180_0002
18/05/18 05:44:24 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.20.193:8020, Ident: (token for thanos: HDFS_DELEGATION_TOKEN owner=thanos/user@NITHINRAOT.SG, renewer=yarn, realUser=, issueDate=1526622264270, maxDate=1527227064270, sequenceNumber=2, masterKeyId=2)
18/05/18 05:44:24 INFO impl.YarnClientImpl: Submitted application application_1526621995180_0002
18/05/18 05:44:25 INFO mapreduce.Job: The url to track the job: http://ip-172-31-20-193.us-east-2.compute.internal:8088/proxy/application_1526621995180_0002/
18/05/18 05:44:25 INFO mapreduce.Job: Running job: job_1526621995180_0002
18/05/18 05:44:41 INFO mapreduce.Job: Job job_1526621995180_0002 running in uber mode : false
18/05/18 05:44:41 INFO mapreduce.Job:  map 0% reduce 0%
18/05/18 05:44:48 INFO mapreduce.Job:  map 100% reduce 0%
18/05/18 05:44:54 INFO mapreduce.Job:  map 100% reduce 100%
18/05/18 05:44:54 INFO mapreduce.Job: Job job_1526621995180_0002 completed successfully
18/05/18 05:44:54 INFO mapreduce.Job: Counters: 49
        File System Counters
                FILE: Number of bytes read=49
                FILE: Number of bytes written=388261
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=600
                HDFS: Number of bytes written=215
                HDFS: Number of read operations=11
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=3
        Job Counters
                Launched map tasks=2
                Launched reduce tasks=1
                Data-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=7417
                Total time spent by all reduces in occupied slots (ms)=3632
                Total time spent by all map tasks (ms)=7417
                Total time spent by all reduce tasks (ms)=3632
                Total vcore-milliseconds taken by all map tasks=7417
                Total vcore-milliseconds taken by all reduce tasks=3632
                Total megabyte-milliseconds taken by all map tasks=7595008
                Total megabyte-milliseconds taken by all reduce tasks=3719168
        Map-Reduce Framework
                Map input records=2
                Map output records=4
                Map output bytes=36
                Map output materialized bytes=67
                Input split bytes=364
                Combine input records=0
                Combine output records=0
                Reduce input groups=2
                Reduce shuffle bytes=67
                Reduce input records=4
                Reduce output records=0
                Spilled Records=8
                Shuffled Maps =2
                Failed Shuffles=0
                Merged Map outputs=2
                GC time elapsed (ms)=165
                CPU time spent (ms)=2080
                Physical memory (bytes) snapshot=1170362368
                Virtual memory (bytes) snapshot=8387420160
                Total committed heap usage (bytes)=1230503936
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=236
        File Output Format Counters
                Bytes Written=97
Job Finished in 30.554 seconds
Estimated value of Pi is 3.50000000000000000000

real    0m33.370s
user    0m7.520s
sys     0m0.465s



 
 


