First line of server log ->
2018-05-17 07:15:30,910 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -D
file.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -D
cmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseP
arNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args
: [], Version: 5.13.3 (#6 built by jenkins on 20180328-1830 git: f90c58536c252d70a23bde6d94514d92a1f111d4)
2018-05-17 07:15:30,991 INFO main:org.mortbay.log: Logging to org.slf4j.impl.Log4jLoggerAdapter(org.mortbay.log) via org.mortbay.log.Slf4jLog
2018-05-17 07:15:31,089 INFO main:org.springframework.context.support.ClassPathXmlApplicationContext: Refreshing org.springframework.context.support.ClassPathXmlApplica
tionContext@30a3107a: startup date [Thu May 17 07:15:31 UTC 2018]; root of context hierarchy
2018-05-17 07:15:31,139 INFO main:org.springframework.beans.factory.xml.XmlBeanDefinitionReader: Loading XML bean definitions from class path resource [webapp/WEB-INF/s
pring/beanRefFactory.xml]


Lines that contains jetty server ->
2018-05-17 07:16:26,286 INFO WebServerImpl:org.mortbay.log: Started SelectChannelConnector@0.0.0.0:7180
2018-05-17 07:16:26,286 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.

