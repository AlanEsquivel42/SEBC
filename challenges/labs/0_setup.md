```
Provider: AWS  
```
```
172.31.5.226	ip-172-31-5-226.ec2.internal
172.31.60.235	ip-172-31-60-235.ec2.internal
172.31.62.160	ip-172-31-62-160.ec2.internal
172.31.57.117	ip-172-31-57-117.ec2.internal
```

<code>[root@ip-172-31-60-72 ec2-user]# cat /etc/redhat-release</code>  
<code>Red Hat Enterprise Linux Server release 7.4 (Maipo)</code>  
  
```
[root@ip-172-31-60-72 ec2-user]# lsblk
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvda    202:0    0   50G  0 disk
├─xvda1 202:1    0    1M  0 part
└─xvda2 202:2    0   50G  0 part /
xvdb    202:16   0  120G  0 disk
└─xvdb1 202:17   0  120G  0 part /data00
xvdc    202:32   0  120G  0 disk
└─xvdc1 202:33   0  120G  0 part /data01
```
  
```

[root@ip-172-31-60-72 ec2-user]# yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
rhui-REGION-client-config-server-7                                                                            | 2.9 kB  00:00:00
https://rhui2-cds02.us-east-1.aws.ce.redhat.com/pulp/repos//content/dist/rhel/rhui/server/7/7Server/x86_64/os/repodata/repomd.xml: [Errno 14] HTTPS Error 401 - Unauthorized
Trying other mirror.
rhui-REGION-rhel-server-releases                                                                              | 3.5 kB  00:00:00
rhui-REGION-rhel-server-rh-common                                                                             | 3.8 kB  00:00:00
(1/7): rhui-REGION-client-config-server-7/x86_64/primary_db                                                   | 6.6 kB  00:00:00
(2/7): rhui-REGION-rhel-server-releases/7Server/x86_64/updateinfo                                             | 2.4 MB  00:00:00
(3/7): rhui-REGION-rhel-server-releases/7Server/x86_64/group                                                  | 709 kB  00:00:00
(4/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/group                                                 |  104 B  00:00:00
(5/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/updateinfo                                            |  32 kB  00:00:00
(6/7): rhui-REGION-rhel-server-rh-common/7Server/x86_64/primary_db                                            | 119 kB  00:00:00
(7/7): rhui-REGION-rhel-server-releases/7Server/x86_64/primary_db                                             |  44 MB  00:00:00
repo id                                                 repo name                                                              status
rhui-REGION-client-config-server-7/x86_64               Red Hat Update Infrastructure 2.0 Client Configuration Server 7             8
rhui-REGION-rhel-server-releases/7Server/x86_64         Red Hat Enterprise Linux Server 7 (RPMs)                               17,521
rhui-REGION-rhel-server-rh-common/7Server/x86_64        Red Hat Enterprise Linux Server 7 RH Common (RPMs)                        228
repolist: 17,757
```
```
[root@ip-172-31-60-72 ec2-user]# cat /etc/passwd | grep haley
haley:x:2900:1001::/home/haley:/bin/bash
[root@ip-172-31-60-72 ec2-user]# cat /etc/passwd | grep saturn
saturn:x:2800:1002::/home/saturn:/bin/bash
[root@ip-172-31-60-72 ec2-user]#
[root@ip-172-31-60-72 ec2-user]# cat /etc/group | grep comets
comets:x:1001:
[root@ip-172-31-60-72 ec2-user]# cat /etc/group | grep planets
planets:x:1002:

```
