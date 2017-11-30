
# Preguntas y respuestas
  
**What is ubertask optimization?**  
If the job is small, the application master may choose to run them in the same JVM as itself, since it judges the overhead of allocating new containers and running tasks in them as outweighing the gain to be had in running them in parallel, compared to running them sequentially on one node. (This is different to Mapreduce 1, where small jobs are never run on a single task tracker.)
  
**Where in CM is the Kerberos Security Realm value displayed?**  
1- Select Administration tab.  
2- Select Settings.  
3- Select Category > Kerberos.  
4- Select Status > Non-default  
  
**Which CDH service(s) host a property for enabling Kerberos authentication?**  
Sentry  
Hue  
Hive  
  
How do you upgrade the CM agents?  
1. Log in to the Cloudera Manager Admin Console.  
  
2. Upgrade hosts using one of the following methods:  
   + Cloudera Manager installs Agent software  
     - Select Yes, I would like to upgrade the Cloudera Manager Agent packages now and click Continue.  
     - Select the release of the Cloudera Manager Agent to install. Normally, this is the Matched Release for this Cloudera Manager Server. However, if you used a custom repository (instead of archive.cloudera.com) for the Cloudera Manager server, select Custom Repository and provide the required information. The custom repository allows you to use an alternative location, but that location must contain the matched Agent version.  
     - Click Continue. The JDK Installation Options page displays.  
Leave Install Oracle Java SE Development Kit (JDK) checked to allow Cloudera Manager to install the JDK on each cluster host, or uncheck if you plan to install it yourself.
If local laws permit you to deploy unlimited strength encryption, and you are running a secure cluster, check the Install Java Unlimited Strength Encryption Policy Files checkbox.
Click Continue.
Specify credentials and initiate Agent installation:
Select root or enter the username for an account that has password-less sudo permission.
Select an authentication method:
If you choose password authentication, enter and confirm the password.
If you choose public-key authentication, provide a passphrase and path to the required key files.
You can specify an alternate SSH port. The default value is 22.
You can specify the maximum number of host installations to run at once. The default value is 10.
Click Continue. The Cloudera Manager Agent packages and optionally the JDK are installed.
Click Continue. The Host Inspector runs to inspect your managed hosts for correct versions and configurations. If there are problems, you can make changes and then rerun the inspector. When you are satisfied with the inspection results, click Continue.
Give the tsquery statement used to chart Hue's CPU utilization?  
Name all the roles that make up the Hive service  
What steps must be completed before integrating Cloudera Manager with Kerberos?  
