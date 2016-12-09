```
[root@clouderaseb00 ~]# df -h
Filesystem            Size  Used Avail Use% Mounted on
/dev/mapper/vg_clouderaseb00-lv_root
                       91G  768M   85G   1% /
tmpfs                  12G     0   12G   0% /dev/shm
/dev/sda1             477M   38M  414M   9% /boot
/dev/sdb1              99G   60M   94G   1% /data1
[root@clouderaseb00 ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.neowiz.com
 * extras: ftp.neowiz.com
 * updates: ftp.neowiz.com
base                                                     | 3.7 kB     00:00
extras                                                   | 3.4 kB     00:00
updates                                                  | 3.4 kB     00:00
repo id                        repo name                                  status
base                           CentOS-6 - Base                            6,696
extras                         CentOS-6 - Extras                             62
updates                        CentOS-6 - Updates                           686
repolist: 7,444
[root@clouderaseb00 ~]# groupadd walks
[root@clouderaseb00 ~]# groupadd shops
[root@clouderaseb00 ~]# useradd -u 2700 -g walks raffles
[root@clouderaseb00 ~]# useradd -u 2800 -g shops orchard
[root@clouderaseb00 ~]# egrep "raffles|orchard" /etc/passwd
raffles:x:2700:500::/home/raffles:/bin/bash
orchard:x:2800:501::/home/orchard:/bin/bash
[root@clouderaseb00 ~]# egrep "walks|shops" /etc/group
walks:x:500:
shops:x:501:
[root@clouderaseb00 ~]#
```

