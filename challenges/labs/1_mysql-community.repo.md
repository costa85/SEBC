## MySQL repo

```
[mysql-connectors-community]
name=MySQL Connectors Community
baseurl=http://repo.mysql.com/yum/mysql-connectors-community/el/6/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

[mysql-tools-community]
name=MySQL Tools Community
baseurl=http://repo.mysql.com/yum/mysql-tools-community/el/6/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

# Enable to use MySQL 5.5
[mysql55-community]
name=MySQL 5.5 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.5-community/el/6/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

# Enable to use MySQL 5.6
[mysql56-community]
name=MySQL 5.6 Community Server
baseurl=http://repo.mysql.com/yum/mysql-5.6-community/el/6/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql

# Note: MySQL 5.7 is currently in development. For use at your own risk.
# Please read with sub pages: https://dev.mysql.com/doc/relnotes/mysql/5.7/en/
[mysql57-community-dmr]
name=MySQL 5.7 Community Server Development Milestone Release
baseurl=http://repo.mysql.com/yum/mysql-5.7-community/el/6/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
```


## Install MySQL 5.5.x server on any node

```
[root@clouderaseb00 ~]# rpm -ivh http://dev.mysql.com/get/mysql-community-release-el6-5.noarch.rpm
Retrieving http://dev.mysql.com/get/mysql-community-release-el6-5.noarch.rpm
Preparing...                ########################################### [100%]
   1:mysql-community-release########################################### [100%]
[root@clouderaseb00 ~]# ll
total 20
-rw-------. 1 root root 1290 Dec  9 10:22 anaconda-ks.cfg
-rw-r--r--. 1 root root 9795 Dec  9 10:22 install.log
-rw-r--r--. 1 root root 3161 Dec  9 10:21 install.log.syslog
[root@clouderaseb00 ~]# cd /etc/yum.repos.d/
[root@clouderaseb00 yum.repos.d]# ll
total 32
-rw-r--r--. 1 root root 1991 Aug  4  2015 CentOS-Base.repo
-rw-r--r--. 1 root root  647 Aug  4  2015 CentOS-Debuginfo.repo
-rw-r--r--. 1 root root  289 Aug  4  2015 CentOS-fasttrack.repo
-rw-r--r--. 1 root root  630 Aug  4  2015 CentOS-Media.repo
-rw-r--r--. 1 root root 6259 Aug  4  2015 CentOS-Vault.repo
-rw-r--r--. 1 root root 1209 Dec  2  2013 mysql-community.repo
-rw-r--r--. 1 root root 1060 Dec  2  2013 mysql-community-source.repo
[root@clouderaseb00 yum.repos.d]# vi mysql-community.repo
[root@clouderaseb00 yum.repos.d]# yum clean all
Loaded plugins: fastestmirror
Cleaning repos: base extras mysql-connectors-community mysql-tools-community
              : mysql55-community updates
Cleaning up Everything
Cleaning up list of fastest mirrors
[root@clouderaseb00 yum.repos.d]# yum repolist
Loaded plugins: fastestmirror
Determining fastest mirrors
 * base: mirror.navercorp.com
 * extras: mirror.navercorp.com
 * updates: mirror.navercorp.com
base                                                     | 3.7 kB     00:00
base/primary_db                                          | 4.7 MB     00:01
extras                                                   | 3.4 kB     00:00
extras/primary_db                                        |  37 kB     00:00
mysql-connectors-community                               | 2.5 kB     00:00
mysql-connectors-community/primary_db                    |  11 kB     00:00
mysql-tools-community                                    | 2.5 kB     00:00
mysql-tools-community/primary_db                         |  33 kB     00:00
mysql55-community                                        | 2.5 kB     00:00
mysql55-community/primary_db                             | 154 kB     00:00
updates                                                  | 3.4 kB     00:00
updates/primary_db                                       | 3.7 MB     00:00
repo id                              repo name                            status
base                                 CentOS-6 - Base                      6,696
extras                               CentOS-6 - Extras                       62
mysql-connectors-community           MySQL Connectors Community              24
mysql-tools-community                MySQL Tools Community                   42
mysql55-community                    MySQL 5.5 Community Server             316
updates                              CentOS-6 - Updates                     686
repolist: 7,826
[root@clouderaseb00 yum.repos.d]# yum search mysql-server
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.navercorp.com
 * extras: mirror.navercorp.com
 * updates: mirror.navercorp.com
========================== N/S Matched: mysql-server ===========================
mysql-server.x86_64 : The MySQL server and related files

  Name and summary matches only, use "search all" for everything.
[root@clouderaseb00 yum.repos.d]# yum install mysql-community-server mysql-community-client mysql-community-libs mysql-community-common
Loaded plugins: fastestmirror
Setting up Install Process
Loading mirror speeds from cached hostfile
 * base: mirror.navercorp.com
 * extras: mirror.navercorp.com
 * updates: mirror.navercorp.com
Resolving Dependencies
--> Running transaction check
---> Package mysql-community-client.x86_64 0:5.5.53-2.el6 will be installed
---> Package mysql-community-common.x86_64 0:5.5.53-2.el6 will be installed
---> Package mysql-community-libs.x86_64 0:5.5.53-2.el6 will be obsoleting
---> Package mysql-community-server.x86_64 0:5.5.53-2.el6 will be installed
--> Processing Dependency: perl(DBI) for package: mysql-community-server-5.5.53-2.el6.x86_64
--> Processing Dependency: libaio.so.1(LIBAIO_0.4)(64bit) for package: mysql-community-server-5.5.53-2.el6.x86_64
--> Processing Dependency: libaio.so.1(LIBAIO_0.1)(64bit) for package: mysql-community-server-5.5.53-2.el6.x86_64
--> Processing Dependency: libaio.so.1()(64bit) for package: mysql-community-server-5.5.53-2.el6.x86_64
---> Package mysql-libs.x86_64 0:5.1.73-5.el6_6 will be obsoleted
--> Processing Dependency: libmysqlclient.so.16()(64bit) for package: 2:postfix-2.6.6-6.el6_5.x86_64
--> Processing Dependency: libmysqlclient.so.16(libmysqlclient_16)(64bit) for package: 2:postfix-2.6.6-6.el6_5.x86_64
--> Running transaction check
---> Package libaio.x86_64 0:0.3.107-10.el6 will be installed
---> Package mysql-community-libs-compat.x86_64 0:5.5.53-2.el6 will be obsoleting
---> Package perl-DBI.x86_64 0:1.609-4.el6 will be installed
---> Package postfix.x86_64 2:2.6.6-6.el6_5 will be updated
---> Package postfix.x86_64 2:2.6.6-6.el6_7.1 will be an update
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package                     Arch   Version             Repository         Size
================================================================================
Installing:
 mysql-community-client      x86_64 5.5.53-2.el6        mysql55-community  15 M
 mysql-community-common      x86_64 5.5.53-2.el6        mysql55-community 277 k
 mysql-community-libs        x86_64 5.5.53-2.el6        mysql55-community 1.7 M
     replacing  mysql-libs.x86_64 5.1.73-5.el6_6
 mysql-community-libs-compat x86_64 5.5.53-2.el6        mysql55-community 1.6 M
     replacing  mysql-libs.x86_64 5.1.73-5.el6_6
 mysql-community-server      x86_64 5.5.53-2.el6        mysql55-community  38 M
Installing for dependencies:
 libaio                      x86_64 0.3.107-10.el6      base               21 k
 perl-DBI                    x86_64 1.609-4.el6         base              705 k
Updating for dependencies:
 postfix                     x86_64 2:2.6.6-6.el6_7.1   base              2.0 M

Transaction Summary
================================================================================
Install       7 Package(s)
Upgrade       1 Package(s)

Total download size: 59 M
Is this ok [y/N]: y
Downloading Packages:
(1/8): libaio-0.3.107-10.el6.x86_64.rpm                  |  21 kB     00:00
(2/8): mysql-community-client-5.5.53-2.el6.x86_64.rpm    |  15 MB     00:01
(3/8): mysql-community-common-5.5.53-2.el6.x86_64.rpm    | 277 kB     00:00
(4/8): mysql-community-libs-5.5.53-2.el6.x86_64.rpm      | 1.7 MB     00:00
(5/8): mysql-community-libs-compat-5.5.53-2.el6.x86_64.r | 1.6 MB     00:00
(6/8): mysql-community-server-5.5.53-2.el6.x86_64.rpm    |  38 MB     00:04
(7/8): perl-DBI-1.609-4.el6.x86_64.rpm                   | 705 kB     00:00
(8/8): postfix-2.6.6-6.el6_7.1.x86_64.rpm                | 2.0 MB     00:00
--------------------------------------------------------------------------------
Total                                           7.9 MB/s |  59 MB     00:07
warning: rpmts_HdrFromFdno: Header V3 DSA/SHA1 Signature, key ID 5072e1f5: NOKEY
Retrieving key from file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
Importing GPG key 0x5072E1F5:
 Userid : MySQL Release Engineering <mysql-build@oss.oracle.com>
 Package: mysql-community-release-el6-5.noarch (installed)
 From   : file:/etc/pki/rpm-gpg/RPM-GPG-KEY-mysql
Is this ok [y/N]: y
Running rpm_check_debug
Running Transaction Test
Transaction Test Succeeded
Running Transaction
Warning: RPMDB altered outside of yum.
  Installing : mysql-community-common-5.5.53-2.el6.x86_64                  1/10
  Installing : mysql-community-libs-5.5.53-2.el6.x86_64                    2/10
  Installing : mysql-community-client-5.5.53-2.el6.x86_64                  3/10
  Installing : mysql-community-libs-compat-5.5.53-2.el6.x86_64             4/10
  Installing : libaio-0.3.107-10.el6.x86_64                                5/10
  Installing : perl-DBI-1.609-4.el6.x86_64                                 6/10
  Installing : mysql-community-server-5.5.53-2.el6.x86_64                  7/10
  Updating   : 2:postfix-2.6.6-6.el6_7.1.x86_64                            8/10
  Cleanup    : 2:postfix-2.6.6-6.el6_5.x86_64                              9/10
  Erasing    : mysql-libs-5.1.73-5.el6_6.x86_64                           10/10
  Verifying  : mysql-community-client-5.5.53-2.el6.x86_64                  1/10
  Verifying  : 2:postfix-2.6.6-6.el6_7.1.x86_64                            2/10
  Verifying  : mysql-community-libs-5.5.53-2.el6.x86_64                    3/10
  Verifying  : mysql-community-common-5.5.53-2.el6.x86_64                  4/10
  Verifying  : perl-DBI-1.609-4.el6.x86_64                                 5/10
  Verifying  : mysql-community-libs-compat-5.5.53-2.el6.x86_64             6/10
  Verifying  : mysql-community-server-5.5.53-2.el6.x86_64                  7/10
  Verifying  : libaio-0.3.107-10.el6.x86_64                                8/10
  Verifying  : mysql-libs-5.1.73-5.el6_6.x86_64                            9/10
  Verifying  : 2:postfix-2.6.6-6.el6_5.x86_64                             10/10

Installed:
  mysql-community-client.x86_64 0:5.5.53-2.el6
  mysql-community-common.x86_64 0:5.5.53-2.el6
  mysql-community-libs.x86_64 0:5.5.53-2.el6
  mysql-community-libs-compat.x86_64 0:5.5.53-2.el6
  mysql-community-server.x86_64 0:5.5.53-2.el6

Dependency Installed:
  libaio.x86_64 0:0.3.107-10.el6          perl-DBI.x86_64 0:1.609-4.el6

Dependency Updated:
  postfix.x86_64 2:2.6.6-6.el6_7.1

Replaced:
  mysql-libs.x86_64 0:5.1.73-5.el6_6

Complete!
[root@clouderaseb00 yum.repos.d]# yum install mysql-server
Loaded plugins: fastestmirror
Setting up Install Process
Loading mirror speeds from cached hostfile
 * base: mirror.navercorp.com
 * extras: mirror.navercorp.com
 * updates: mirror.navercorp.com
Package mysql-server-5.1.73-7.el6.x86_64 is obsoleted by mysql-community-server-5.5.53-2.el6.x86_64 which is already installed
Nothing to do
[root@clouderaseb00 yum.repos.d]#

```