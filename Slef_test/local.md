```
[root@c02n2t ~]# cat /etc/yum.repos.d/local.repo 
[centos]
name=centos
baseurl=http://10.10.10.254/centos/x86_64/7.2/
enabled=1
gpgcheck=0

[gangpbs]
name=progang
baseurl=http://10.10.10.254/centos/x86_64/7.2_extras/
enabled=1
gpgcheck=0

[root@c02n2t ~]# 
```