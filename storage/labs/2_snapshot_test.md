## <center> <a name="Hdfs: Snapshot"/> HDFS Lab: Test HDFS Snapshots
* hadoop fs -mkdir /user/nithinraot/precious
* hadoop fs -put jclouds-compute-1.7.1.jar /user/nithinraot/precious/
* enable snapshot & take snap shot of the required directory. In this case, I had taken the snapshot of entire "/" directory. we can also take it for one specific directory.
* now we can delete the new file that is pushed into the hdfs directory -> hadoop fs -rm /user/nithinraot/precious/jclouds-compute-1.7.1.jar
* snapshot file is availbale under "/.snapshot/sebc-hdfs-test/user/nithinraot/precious"
* hadoop fs -cp -ptopax /.snapshot/sebc-hdfs-test/user/nithinraot/precious/jclouds-compute-1.7.1.jar /user/nithinraot/precious/