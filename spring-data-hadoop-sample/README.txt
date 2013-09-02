esta dando una excepcion, http://stackoverflow.com/questions/15786155/sppring-data-hadoop-map-reduce-job-thrwoing-no-class-found-exception?noredirect=1#comment22445005_15786155

Tienes hadoop instalado y funcionando en modo distribuido simulado :)

enlaces de interes:

http://bigdatastudio.com/2012/12/06/how-can-i-learn-hadoop/

http://www.adictosaltrabajo.com/tutoriales/tutoriales.php?pagina=hadoop

http://www.adictosaltrabajo.com/tutoriales/tutoriales.php?pagina=hadoopFS

http://localhost:50070/dfshealth.jsp

http://localhost:50030/jobtracker.jsp

http://www.petrikainulainen.net/programming/apache-hadoop/creating-hadoop-mapreduce-job-with-spring-data-apache-hadoop/

http://www.petrikainulainen.net/programming/tips-and-tricks/creating-a-runnable-binary-distribution-with-maven-assembly-plugin/

http://www.petrikainulainen.net/programming/apache-hadoop/creating-hadoop-mapreduce-job-with-spring-data-apache-hadoop/

http://blog.guident.com/2013/01/spring-into-apache-hadoop/

http://www.swatcloud.com


13/08/19 16:22:40 INFO support.ClassPathXmlApplicationContext: Refreshing org.springframework.context.support.ClassPathXmlApplicationContext@26fd68b1: startup date [Mon Aug 19 16:22:40 CEST 2013]; root of context hierarchy
13/08/19 16:22:40 INFO xml.XmlBeanDefinitionReader: Loading XML bean definitions from class path resource [META-INF/spring/app-context.xml]
13/08/19 16:22:41 INFO config.PropertyPlaceholderConfigurer: Loading properties file from class path resource [application.properties]
13/08/19 16:22:41 INFO support.DefaultListableBeanFactory: Pre-instantiating singletons in org.springframework.beans.factory.support.DefaultListableBeanFactory@688a548b: defining beans [exampleService,wordMapper,wordReducer,org.springframework.context.annotation.internalConfigurationAnnotationProcessor,org.springframework.context.annotation.internalAutowiredAnnotationProcessor,org.springframework.context.annotation.internalRequiredAnnotationProcessor,org.springframework.context.annotation.internalCommonAnnotationProcessor,org.springframework.beans.factory.config.PropertyPlaceholderConfigurer#0,hadoopConfiguration,wordCountJob,wordCountJobRunner]; root of factory hierarchy
2013-08-19 16:22:42.031 java[5645:1903] Unable to load realm info from SCDynamicStore
13/08/19 16:22:42 INFO mapreduce.JobRunner: Starting job [wordCountJob]
13/08/19 16:22:43 WARN mapred.JobClient: No job jar file set.  User classes may not be found. See JobConf(Class) or JobConf#setJar(String).
13/08/19 16:22:43 INFO input.FileInputFormat: Total input paths to process : 1
13/08/19 16:22:43 WARN util.NativeCodeLoader: Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
13/08/19 16:22:43 WARN snappy.LoadSnappy: Snappy native library not loaded
13/08/19 16:22:43 INFO mapred.JobClient: Running job: job_201308191610_0004
13/08/19 16:22:44 INFO mapred.JobClient:  map 0% reduce 0%
13/08/19 16:22:58 INFO mapred.JobClient: Task Id : attempt_201308191610_0004_m_000000_0, Status : FAILED
java.lang.RuntimeException: java.lang.ClassNotFoundException: org.aironman.hadoop.WordMapper
	at org.apache.hadoop.conf.Configuration.getClass(Configuration.java:857)
	at org.apache.hadoop.mapreduce.JobContext.getMapperClass(JobContext.java:199)
	at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:718)
	at org.apache.hadoop.mapred.MapTask.run(MapTask.java:364)
	at org.apache.hadoop.mapred.Child$4.run(Child.java:255)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:396)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1190)
	at org.apache.hadoop.mapred.Child.main(Child.java:249)
Caused by: java.lang.ClassNotFoundException: org.aironman.hadoop.WordMapper
	at java.net.URLClassLoader$1.run(URLClassLoader.java:202)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.net.URLClassLoader.findClass(URLClassLoader.java:190)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:306)
	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:301)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:247)
	at java.lang.Class.forName0(Native Method)
	at java.lang.Class.forName(Class.java:249)
	at org.apache.hadoop.conf.Configuration.getClassByName(Configuration.java:810)
	at org.apache.hadoop.conf.Configuration.getClass(Configuration.java:855)
	... 8 more

attempt_201308191610_0004_m_000000_0: 2013-08-19 16:22:51.862 java[5658:1903] Unable to load realm info from SCDynamicStore
13/08/19 16:23:07 INFO mapred.JobClient: Task Id : attempt_201308191610_0004_m_000000_1, Status : FAILED
java.lang.RuntimeException: java.lang.ClassNotFoundException: org.aironman.hadoop.WordMapper
	at org.apache.hadoop.conf.Configuration.getClass(Configuration.java:857)
	at org.apache.hadoop.mapreduce.JobContext.getMapperClass(JobContext.java:199)
	at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:718)
	at org.apache.hadoop.mapred.MapTask.run(MapTask.java:364)
	at org.apache.hadoop.mapred.Child$4.run(Child.java:255)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:396)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1190)
	at org.apache.hadoop.mapred.Child.main(Child.java:249)
Caused by: java.lang.ClassNotFoundException: org.aironman.hadoop.WordMapper
	at java.net.URLClassLoader$1.run(URLClassLoader.java:202)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.net.URLClassLoader.findClass(URLClassLoader.java:190)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:306)
	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:301)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:247)
	at java.lang.Class.forName0(Native Method)
	at java.lang.Class.forName(Class.java:249)
	at org.apache.hadoop.conf.Configuration.getClassByName(Configuration.java:810)
	at org.apache.hadoop.conf.Configuration.getClass(Configuration.java:855)
	... 8 more

attempt_201308191610_0004_m_000000_1: 2013-08-19 16:23:00.439 java[5677:1903] Unable to load realm info from SCDynamicStore
13/08/19 16:23:15 INFO mapred.JobClient: Task Id : attempt_201308191610_0004_m_000000_2, Status : FAILED
java.lang.RuntimeException: java.lang.ClassNotFoundException: org.aironman.hadoop.WordMapper
	at org.apache.hadoop.conf.Configuration.getClass(Configuration.java:857)
	at org.apache.hadoop.mapreduce.JobContext.getMapperClass(JobContext.java:199)
	at org.apache.hadoop.mapred.MapTask.runNewMapper(MapTask.java:718)
	at org.apache.hadoop.mapred.MapTask.run(MapTask.java:364)
	at org.apache.hadoop.mapred.Child$4.run(Child.java:255)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:396)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1190)
	at org.apache.hadoop.mapred.Child.main(Child.java:249)
Caused by: java.lang.ClassNotFoundException: org.aironman.hadoop.WordMapper
	at java.net.URLClassLoader$1.run(URLClassLoader.java:202)
	at java.security.AccessController.doPrivileged(Native Method)
	at java.net.URLClassLoader.findClass(URLClassLoader.java:190)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:306)
	at sun.misc.Launcher$AppClassLoader.loadClass(Launcher.java:301)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:247)
	at java.lang.Class.forName0(Native Method)
	at java.lang.Class.forName(Class.java:249)
	at org.apache.hadoop.conf.Configuration.getClassByName(Configuration.java:810)
	at org.apache.hadoop.conf.Configuration.getClass(Configuration.java:855)
	... 8 more

attempt_201308191610_0004_m_000000_2: 2013-08-19 16:23:08.913 java[5697:1903] Unable to load realm info from SCDynamicStore
13/08/19 16:23:28 INFO mapred.JobClient: Job complete: job_201308191610_0004
13/08/19 16:23:28 INFO mapred.JobClient: Counters: 7
13/08/19 16:23:28 INFO mapred.JobClient:   Job Counters 
13/08/19 16:23:28 INFO mapred.JobClient:     SLOTS_MILLIS_MAPS=41725
13/08/19 16:23:28 INFO mapred.JobClient:     Total time spent by all reduces waiting after reserving slots (ms)=0
13/08/19 16:23:28 INFO mapred.JobClient:     Total time spent by all maps waiting after reserving slots (ms)=0
13/08/19 16:23:28 INFO mapred.JobClient:     Launched map tasks=4
13/08/19 16:23:28 INFO mapred.JobClient:     Data-local map tasks=4
13/08/19 16:23:28 INFO mapred.JobClient:     SLOTS_MILLIS_REDUCES=0
13/08/19 16:23:28 INFO mapred.JobClient:     Failed map tasks=1
13/08/19 16:23:28 INFO mapreduce.JobRunner: Completed job [wordCountJob]
13/08/19 16:23:28 INFO support.DefaultListableBeanFactory: Destroying singletons in org.springframework.beans.factory.support.DefaultListableBeanFactory@688a548b: defining beans [exampleService,wordMapper,wordReducer,org.springframework.context.annotation.internalConfigurationAnnotationProcessor,org.springframework.context.annotation.internalAutowiredAnnotationProcessor,org.springframework.context.annotation.internalRequiredAnnotationProcessor,org.springframework.context.annotation.internalCommonAnnotationProcessor,org.springframework.beans.factory.config.PropertyPlaceholderConfigurer#0,hadoopConfiguration,wordCountJob,wordCountJobRunner]; root of factory hierarchy
Exception in thread "main" org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'wordCountJobRunner': Invocation of init method failed; nested exception is java.lang.IllegalStateException: Job wordCountJob] failed to start; status=FAILED
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1420)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:519)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:456)
	at org.springframework.beans.factory.support.AbstractBeanFactory$1.getObject(AbstractBeanFactory.java:293)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:222)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:290)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:192)
	at org.springframework.beans.factory.support.DefaultListableBeanFactory.preInstantiateSingletons(DefaultListableBeanFactory.java:585)
	at org.springframework.context.support.AbstractApplicationContext.finishBeanFactoryInitialization(AbstractApplicationContext.java:895)
	at org.springframework.context.support.AbstractApplicationContext.refresh(AbstractApplicationContext.java:425)
	at org.springframework.context.support.ClassPathXmlApplicationContext.<init>(ClassPathXmlApplicationContext.java:139)
	at org.springframework.context.support.ClassPathXmlApplicationContext.<init>(ClassPathXmlApplicationContext.java:83)
	at org.aironman.hadoop.Main.main(Main.java:8)
Caused by: java.lang.IllegalStateException: Job wordCountJob] failed to start; status=FAILED
	at org.springframework.data.hadoop.mapreduce.JobExecutor$2.run(JobExecutor.java:219)
	at org.springframework.core.task.SyncTaskExecutor.execute(SyncTaskExecutor.java:48)
	at org.springframework.data.hadoop.mapreduce.JobExecutor.startJobs(JobExecutor.java:168)
	at org.springframework.data.hadoop.mapreduce.JobExecutor.startJobs(JobExecutor.java:160)
	at org.springframework.data.hadoop.mapreduce.JobRunner.call(JobRunner.java:52)
	at org.springframework.data.hadoop.mapreduce.JobRunner.afterPropertiesSet(JobRunner.java:44)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.invokeInitMethods(AbstractAutowireCapableBeanFactory.java:1477)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.initializeBean(AbstractAutowireCapableBeanFactory.java:1417)

	... 12 more