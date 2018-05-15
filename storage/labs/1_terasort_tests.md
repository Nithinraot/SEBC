<div style="page-break-after: always;"></div>
## <center> <a name="Hdfs: Throughput"/> HDFS Lab: Test HDFS throughput
* Teragen
<code>time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.14.2.jar teragen -D dfs.block.size=33554432 -Dmapreduce.job.maps=4 10000000 /user/nithinraot/teragen/ </code>
* Output
----real 0m19.456s
----user 0m6.967s
----sys 0m0.339s

<code>time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.14.2.jar terasort /user/nithinraot/teragen/ /user/nithinraot/terasort/ </code>
* Output
----real 0m53.992s
----user 0m8.958s
----sys 0m0.432s

---
<div style="page-break-after: always;"></div>