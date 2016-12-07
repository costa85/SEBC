* What is ubertask optimization?

   * Which is enable ubertask optimization, which runs “sufficiently small” jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings. This property can be changed in Performance category. Property name is mapreduce.job.ubertask.enable

* Where in CM is the Kerberos Security Realm value displayed?

   * CM Search Bar -> type Kerberos Security Realm

* Which CDH service(s) host a property for enabling Kerberos authentication?

   * CM Search Bar -> type Enable Kerberos
      * Zookeeper: Enable Kerberos Authentication
      * HDFS: Enable Kerberos Authentication for HTTP Web-consoles
      * YARN: Enable Kerberos Authentication for HTTP Web-consoles

* How do you upgrade the CM agents?

   * Using Upgrade Wizard
   * This is a link to [Upgrading Cloudera Manager](http://www.cloudera.com/documentation/enterprise/latest/topics/cm_ag_ug_cm5.html)

* Give the tsquery statement used to chart Hue's CPU utilization?

   * SELECT cpu_system_rate + cpu_user_rate WHERE serviceType = HUE AND category = ROLE

* Name all the roles that make up the Hive service

   * CM Search Bar -> type role hive
		* HiveServer2
		* Hive Metastore Service
		* Gateway

* What steps must be completed before integrating Cloudera Manager with Kerberos?

	* ![](https://github.com/costa85/SEBC/blob/master/enterprise/labs/beforekerberos.png)
		* Set up a working KDC
		* Checked that the KDC allows renewable tickets
		* OpenLdap client libraries should be installed on the Cloudera Manager Server host
		* Created a proper account for Cloudera Manager

