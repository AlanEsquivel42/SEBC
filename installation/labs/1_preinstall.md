**Prerrequisitos de instalación**
  
sudo lsblk  
sudo parted /dev/xvdb mklabel gpt  
sudo parted /dev/xvdc mklabel gpt  
sudo parted -a opt /dev/xvdb mkpart primary ext4 0% 100%  
sudo parted -a opt /dev/xvdc mkpart primary ext4 0% 100%  
sudo mkfs.ext4 -L datapartition /dev/xvdb1  
sudo mkfs.ext4 -L datapartition /dev/sxvdc1  
vi /etc/fstab  
  
/dev/xvdb1 /data00 ext4 defaults,noatime 1 2
/dev/xvdc1 /data01 ext4 defaults,noatime 1 2
  
sudo mkdir -p /data00  
sudo mkdir -p /data01  
sudo mount -o defaults /dev/xvdb1 /data00  
sudo mount -o defaults /dev/xvdc1 /data01  
sudo lsblk  
  
sudo su  
echo "vm.swappiness = 1" >> /etc/sysctl.conf  
echo 1 > /proc/sys/vm/swappiness  
  
yum install y ntp  
systemctl enable ntpd  
systemctl start ntpd  
ntpq -p  
  
systemctl status firewalld.service  
systemctl stop firewalld.service  
systemctl disable firewalld.service  
  
selinuxenabled || echo "disabled"  
reboot  
sestatus  
  
vi /etc/rc.local  
echo never > /sys/kernel/mm/transparent_hugepage/defrag  
echo never > /sys/kernel/mm/transparent_hugepage/enabled  
sudo chmod a+x /etc/rc.d/rc.local && sudo /etc/rc.d/rc.local  
  
yum install -y wget  
wget http://archive.cloudera.com/cm5/redhat/7/x86_64/cm/5.10.2/RPMS/x86_64/oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm  
rpm -ivh oracle-j2sdk1.7-1.7.0+update67-1.x86_64.rpm  
  
vi /etc/hosts  
  
172.31.20.9 ip-172-31-20-9.ec2.internal nodo1  
172.31.6.221 ip-172-31-6-221.ec2.internal nodo2  
172.31.9.209 ip-172-31-9-209.ec2.internal nodo3  
172.31.8.216 ip-172-31-8-216.ec2.internal nodo4  
  
vi /etc/sysctl.conf  
  
#disable ipv6  
net.ipv6.conf.all.disable_ipv6 = 1  
net.ipv6.conf.default.disable_ipv6 = 1  
net.ipv6.conf.lo.disable_ipv6 = 1  
  
sysctl -p  
  
  