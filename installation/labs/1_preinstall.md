**Prerrequisitos de instalación**
    
<code>sudo parted /dev/xvdb mklabel gpt</code>  
<code>sudo parted /dev/xvdc mklabel gpt</code>  
<code>sudo parted -a opt /dev/xvdb mkpart primary ext4 0% 100%</code>  
<code>sudo parted -a opt /dev/xvdc mkpart primary ext4 0% 100%</code>  
<code>sudo mkfs.ext4 -L datapartition /dev/xvdb1</code>  
<code>sudo mkfs.ext4 -L datapartition /dev/sxvdc1</code>  
<code>vi /etc/fstab</code>  
  
/dev/xvdb1 /data00 ext4 defaults,noatime 1 2  
/dev/xvdc1 /data01 ext4 defaults,noatime 1 2  

![fstab](https://github.com/AlanEsquivel42/SEBC/blob/master/installation/labs/fstab.PNG)  
  
<code>sudo mkdir -p /data00</code>  
<code>sudo mkdir -p /data01</code>  
<code>sudo mount -o defaults /dev/xvdb1 /data00</code>  
<code>sudo mount -o defaults /dev/xvdc1 /data01</code>  
<code>sudo lsblk</code>  
  
![fstab](https://github.com/AlanEsquivel42/SEBC/blob/master/installation/labs/lsblk.PNG)    
  
<code>sudo su</code>  
<code>echo "vm.swappiness = 1" >> /etc/sysctl.conf</code>  
<code>echo 1 > /proc/sys/vm/swappiness</code>  
  
![swap](https://github.com/AlanEsquivel42/SEBC/blob/master/installation/labs/swap.PNG)  
  
<code>yum install y ntp</code>  
<code>systemctl enable ntpd</code>  
<code>systemctl start ntpd</code>  
  
<code>systemctl status firewalld.service</code>  
<code>systemctl stop firewalld.service</code>  
<code>systemctl disable firewalld.service</code>  
  
<code>selinuxenabled || echo "disabled"</code>  
<code>reboot</code>  
<code>sestatus</code>  
  
![sestatus](https://github.com/AlanEsquivel42/SEBC/blob/master/installation/labs/sestatus.PNG)  
  
<code>vi /etc/rc.local  
echo never > /sys/kernel/mm/transparent_hugepage/defrag  
echo never > /sys/kernel/mm/transparent_hugepage/enabled  
    
![rclocal](https://github.com/AlanEsquivel42/SEBC/blob/master/installation/labs/rclocal.PNG)  
  
<code>sudo chmod a+x /etc/rc.d/rc.local && sudo /etc/rc.d/rc.local</code>  
  
<code>yum install -y wget</code>  
<code>wget http://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.10.2/RPMS/x86_64/oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm</code>  
<code>rpm -ivh oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm</code>  
  
<code>vi /etc/hosts</code>  
  
![hosts](https://github.com/AlanEsquivel42/SEBC/blob/master/installation/labs/etchosts.PNG)  
  
<code>vi /etc/sysctl.conf</code>  
  
![sysctl](https://github.com/AlanEsquivel42/SEBC/blob/master/installation/labs/sysctlconf.PNG)      
  
<code>sysctl -p</code>  
  
<code>cat /etc/sysconfig/network-scripts/ifcfg-eth0</code>  
  
<code>nslookup ip-172-31-9-209.ec2.internal</code>  
<code>dig -x 172.31.0.2</code>  
  
 ![nslookup](https://github.com/AlanEsquivel42/SEBC/blob/master/installation/labs/nslookup.PNG)
