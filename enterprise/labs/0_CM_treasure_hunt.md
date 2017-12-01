
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
HDFS  
Impala  
Solr  
Kafka  
  
**How do you upgrade the CM agents?**  
1. Log in to the Cloudera Manager Admin Console.  
  
2. Upgrade hosts using one of the following methods:  
   + Cloudera Manager installs Agent software  
      - Select Yes, I would like to upgrade the Cloudera Manager Agent packages now and click Continue.  
      - Select the release of the Cloudera Manager Agent to install. Normally, this is the Matched Release for this Cloudera Manager    
      Server. However, if you used a custom repository (instead of archive.cloudera.com) for the Cloudera Manager server, select Custom 
      Repository and provide the required information. The custom repository allows you to use an alternative location, but that 
      location must contain the matched Agent version.  
     - Click Continue. The JDK Installation Options page displays.  
        * Leave Install Oracle Java SE Development Kit (JDK) checked to allow Cloudera Manager to install the JDK on each cluster host,           or uncheck if you plan to install it yourself.
        * If local laws permit you to deploy unlimited strength encryption, and you are running a secure cluster, check the Install Java           Unlimited Strength Encryption Policy Files checkbox.
     Click Continue.
     - Specify credentials and initiate Agent installation:
       * Select root or enter the username for an account that has password-less sudo permission.
       * Select an authentication method:
          * If you choose password authentication, enter and confirm the password.
          * If you choose public-key authentication, provide a passphrase and path to the required key files.
       * You can specify an alternate SSH port. The default value is 22.
       * You can specify the maximum number of host installations to run at once. The default value is 10.
      - Click Continue. The Cloudera Manager Agent packages and optionally the JDK are installed.
        Click Continue. The Host Inspector runs to inspect your managed hosts for correct versions and configurations. If there are             problems, you can make changes and then rerun the inspector. When you are satisfied with the inspection results, click Continue.

**Give the tsquery statement used to chart Hue's CPU utilization?**  
    SELECT cpu_percent_across_hosts WHERE serviceType=HUE  
  
**Name all the roles that make up the Hive service**  
    - Hive Metastore Server
    - WebHCat Server
    - HiveServer2
    - Gateway


**What steps must be completed before integrating Cloudera Manager with Kerberos?**  
  
  To install packages for a Kerberos server:  
  <code>yum -y install krb5-server krb5-libs krb5-auth-dialog krb5-workstation</code>
  
  To install packages for a Kerberos client:  
  <code>yum -y install krb5-workstation krb5-libs krb5-auth-dialog</code>
  
  *Server
  
  # vim /var/kerberos/krb5kdc/kdc.conf
  ```
[kdcdefaults]
 kdc_ports = 88
 kdc_tcp_ports = 88

[realms]
  ALANESQUIVEL.COM = {
  #master_key_type = aes256-cts
  acl_file = /var/kerberos/krb5kdc/kadm5.acl
  dict_file = /usr/share/dict/words
  admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
  supported_enctypes = aes256-cts:normal aes128-cts:normal des3-hmac-sha1:normal arcfour-hmac:normal des-hmac-sha1:normal des-cbc-md5:normal des-cbc-crc:normal
  max_life = 1d
  max_renewable_life = 7d
 }
 ```
 
 *All Clients
 
  # vim /etc/krb5.conf
 ```
 
[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = ALANESQUIVEL.COM
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true
 udp_preference_limit = 1
 default_tgs_enctypes = arcfour-hmac
 default_tkt_enctypes = arcfour-hmac 

[realms] 
  ALANESQUIVEL.COM = {
  kdc = ip-172-31-9-209.ec2.internal
  admin_server = ip-172-31-9-209.ec2.internal
 }

[domain_realm]
   .ec2.internal.com = ALANESQUIVEL.COM
   ec2.internal.com = ALANESQUIVEL.COM
   ```
   
   *Create the database using the kdb5_util utility. (Server)
   
   # /usr/sbin/kdb5_util create -s
   ``` 
   Loading random data
   Initializing database '/var/kerberos/krb5kdc/principal' for realm 'ALANESQUIVEL.COM',
   master key name 'K/M@ALANESQUIVEL.COM'
   You will be prompted for the database Master Password.
   It is important that you NOT FORGET this password.
   Enter KDC database master key:
   Re-enter KDC database master key to verify:
   ```
   
   *In Server, add cloudera-scm principal, it will be used by Cloudera Manager later to manage Hadoop principals.
  
   <code># kadmin.local</code>
   ```
   kadmin.local:  addprinc cloudera-scm@ALANESQUIVEL.COM
   WARNING: no policy specified for cloudera-scm@ALANESQUIVEL.COM; defaulting to no policy
   Enter password for principal "cloudera-scm@ALANESQUIVEL.COM":
   Re-enter password for principal "cloudera-scm@ALANESQUIVEL.COM":
   Principal "cloudera-scm@ALANESQUIVEL.COM" created.
   ```
   
   *Add */admin and cloudera-scm to ACL(Access Control List), which gives privilege to add principals for admin and cloudera-scm  
   principal
   
   <code># vim /var/kerberos/krb5kdc/kadm5.acl</code>  
   ``` 
    */admin@ALANESQUIVEL.COM *
    cloudera-scm@ALANESQUIVEL.COM admilc
   ```
   
   *Adds the password policy to the database.  
   
   ```
   # kadmin.local
    kadmin.local:  addpol admin
    kadmin.local:  addpol users
    kadmin.local:  addpol hosts
    kadmin.local:  exit
   ```
   
   *Start Kerberos using the following commands:  
   
   <code>#service krb5kdc start</code>
   <code>#service kadmin start</code>
   
