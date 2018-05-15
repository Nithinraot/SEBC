## <center> <a name="Hdfs: Throughput"/> HDFS Lab: Test HDFS throughput
* Teragen
`time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.14.2.jar teragen -D dfs.block.size=33554432 -Dmapreduce.job.maps=4 10000000 /user/nithinraot/teragen/`
* Output
----real 0m19.456s
----user 0m6.967s
----sys 0m0.339s

* HDFS output file ->

-rw-r--r--   3 nithinraot supergroup          0 2018-05-15 03:35 /user/nithinraot/teragen/_SUCCESS
-rw-r--r--   3 nithinraot supergroup  250000000 2018-05-15 03:35 /user/nithinraot/teragen/part-m-00000
-rw-r--r--   3 nithinraot supergroup  250000000 2018-05-15 03:35 /user/nithinraot/teragen/part-m-00001
-rw-r--r--   3 nithinraot supergroup  250000000 2018-05-15 03:35 /user/nithinraot/teragen/part-m-00002
-rw-r--r--   3 nithinraot supergroup  250000000 2018-05-15 03:35 /user/nithinraot/teragen/part-m-00003

* Terasort
`time hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.14.2.jar terasort /user/nithinraot/teragen/ /user/nithinraot/terasort/ `
* Output
----real 0m53.992s
----user 0m8.958s
----sys 0m0.432s

* HDFS output Terasort ->
*-rw-r--r--   1 nithinraot supergroup          0 2018-05-15 03:36 /user/nithinraot/terasort/_SUCCESS
*-rw-r--r--  10 nithinraot supergroup         77 2018-05-15 03:35 /user/nithinraot/terasort/_partition.lst
*-rw-r--r--   1 nithinraot supergroup  125682500 2018-05-15 03:36 /user/nithinraot/terasort/part-r-00000
*-rw-r--r--   1 nithinraot supergroup  124567300 2018-05-15 03:36 /user/nithinraot/terasort/part-r-00001
-rw-r--r--   1 nithinraot supergroup  125740300 2018-05-15 03:36 /user/nithinraot/terasort/part-r-00002
-rw-r--r--   1 nithinraot supergroup  125777100 2018-05-15 03:36 /user/nithinraot/terasort/part-r-00003
-rw-r--r--   1 nithinraot supergroup  123369100 2018-05-15 03:36 /user/nithinraot/terasort/part-r-00004
-rw-r--r--   1 nithinraot supergroup  125863400 2018-05-15 03:36 /user/nithinraot/terasort/part-r-00005
-rw-r--r--   1 nithinraot supergroup  124362700 2018-05-15 03:36 /user/nithinraot/terasort/part-r-00006
-rw-r--r--   1 nithinraot supergroup  124637600 2018-05-15 03:36 /user/nithinraot/terasort/part-r-00007
