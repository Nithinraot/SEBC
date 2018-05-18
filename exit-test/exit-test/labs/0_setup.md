## <center> Create the Issue Exit-test: Setup
* List of IP address and FQDN ->
 ec2-18-191-59-135.us-east-2.compute.amazonaws.com	CM	ip-172-31-25-114.us-east-2.compute.internal
 ec2-18-216-145-220.us-east-2.compute.amazonaws.com	NN	ip-172-31-20-193.us-east-2.compute.internal
ec2-18-191-114-187.us-east-2.compute.amazonaws.com	SN	 ip-172-31-28-168.us-east-2.compute.internal
ec2-18-191-16-209.us-east-2.compute.amazonaws.com	DN1	ip-172-31-31-10.us-east-2.compute.internal
ec2-18-218-106-124.us-east-2.compute.amazonaws.com	DN2	ip-172-31-24-103.us-east-2.compute.internal

* File size ->
df -h
Filesystem Size Used Avail Use% Mounted on
/dev/xvda2 50G 1.3G 49G 3% /

* Linux version ->
[root@ip-172-31-25-114 ec2-user]# cat /etc/os-release
NAME="Red Hat Enterprise Linux Server"
VERSION="7.5 (Maipo)"
ID="rhel"
ID_LIKE="fedora"
VARIANT="Server"
VARIANT_ID="server"
VERSION_ID="7.5"
PRETTY_NAME="Red Hat Enterprise Linux Server 7.5 (Maipo)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:redhat:enterprise_linux:7.5:GA:server"
HOME_URL="https://www.redhat.com/"
BUG_REPORT_URL="https://bugzilla.redhat.com/"

REDHAT_BUGZILLA_PRODUCT="Red Hat Enterprise Linux 7"
REDHAT_BUGZILLA_PRODUCT_VERSION=7.5
REDHAT_SUPPORT_PRODUCT="Red Hat Enterprise Linux"
REDHAT_SUPPORT_PRODUCT_VERSION="7.5"


* Yum repolist

[root@ip-172-31-25-114 ec2-user]# yum repolist enabled
Loaded plugins: amazon-id, rhui-lb, search-disabled-repos
repo id repo name status
rhui-REGION-client-config-server-7/x86_64 Red Hat Update Infrastructure 2.0 Client Configuration Server 7 2
rhui-REGION-rhel-server-releases/7Server/x86_64 Red Hat Enterprise Linux Server 7 (RPMs) 20,399
rhui-REGION-rhel-server-rh-common/7Server/x86_64 Red Hat Enterprise Linux Server 7 RH Common (RPMs) 231
repolist: 20,632

* Linux accounts to all nodes
[root@ip-172-31-31-10 ec2-user]# tail -4 /etc/passwd
ntp❌38:38::/etc/ntp:/sbin/nologin
thanos❌2500:2500::/home/thanos:/bin/bash
hulk❌2600:2600::/home/hulk:/bin/bash
groot❌2700:2700::/home/groot:/bin/bash

[root@ip-172-31-25-114 ec2-user]# tail -4 /etc/group
hulk❌2600:
groot❌2700:
blackorder❌2701:thanos
avengers❌2702:groot,hulk



