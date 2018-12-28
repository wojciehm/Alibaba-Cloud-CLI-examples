# Table of Contents
=================

   * [Table of Content ECS](#table-of-content-ecs)
   * [One liner to get all images ID sorted out by OS Name, Platorm, OS Type, Architecture and ImageID](#one-liner-to-get-all-images-id-sorted-out-by-os-name-platorm-os-type-architecture-and-imageid)
   * [Result](#result)
   * [One liner to get images from Alibaba Cloud Marketplace](#one-liner-to-get-images-from-alibaba-cloud-marketplace)
   * [Result](#result-1)
   * [One liner to get all ECS instance type in the configure region in your settings.](#one-liner-to-get-all-ecs-instance-type-in-the-configure-region-in-your-settings)
   * [Result](#result-2)
   * [One liner to get list of instances with name, CPU, Memory, OS Name and Status](#one-liner-to-get-list-of-instances-with-name-cpu-memory-os-name-and-status)
   * [Result](#result-3)
   * [One line to start ECS instance from command line](#one-line-to-start-ecs-instance-from-command-line)
   * [One liner to get list of instances with Hostname and Network Interfaces](#one-liner-to-get-list-of-instances-with-hostname-and-network-interfaces)
   * [Result](#result-4)


### One liner to get all images ID sorted out by OS Name, Platorm, OS Type, Architecture and ImageID

`aliyun ecs DescribeImages --RegionId eu-central-1 --ImageOwnerAlias system --output cols=ImageName,ImageId,Platform`

### Result

```bash
ImageName                                          | ImageId                                            | Platform
---------                                          | -------                                            | --------
winsvr_64_dtcC_1709_zh-cn_40G_alibase_20171115.vhd | winsvr_64_dtcC_1709_zh-cn_40G_alibase_20171115.vhd | Windows Server 2016
winsvr_64_dtcC_1709_en-us_40G_alibase_20171115.vhd | winsvr_64_dtcC_1709_en-us_40G_alibase_20171115.vhd | Windows Server 2016
ubuntu_16_0402_64_20G_alibase_20180409.vhd         | ubuntu_16_0402_64_20G_alibase_20180409.vhd         | Ubuntu
ubuntu_16_0402_32_20G_alibase_20180409.vhd         | ubuntu_16_0402_32_20G_alibase_20180409.vhd         | Ubuntu
opensuse_42_03_64_20G_alibase_20171031.vhd         | opensuse_42_03_64_20G_alibase_20171031.vhd         | openSUSE
debian_9_02_64_20G_alibase_20171023.vhd            | debian_9_02_64_20G_alibase_20171023.vhd            | Debian
coreos_1745_7_0_64_30G_alibase_20180705.vhd        | coreos_1745_7_0_64_30G_alibase_20180705.vhd        | CoreOS
centos_7_04_64_20G_alibase_20180419.vhd            | centos_7_04_64_20G_alibase_20180419.vhd            | CentOS
centos_6_09_64_20G_alibase_20180326.vhd            | centos_6_09_64_20G_alibase_20180326.vhd            | CentOS
alinux_17_01_64_20G_cloudinit_20171222.vhd         | alinux_17_01_64_20G_cloudinit_20171222.vhd         | Aliyun
```

### One liner to get images from Alibaba Cloud Marketplace

`aliyun ecs DescribeImages --RegionId eu-central-1 --ImageOwnerAlias marketplace --output cols=ImageName,ImageId,Platform`

### Result

```bash
ImageName                                            | ImageId                | Platform
---------                                            | -------                | --------
Drupal_LEMP_CentOS_7.2_64bit_v1.0 powered by IGS 1.0 | m-gw82urgd458pc6i9gb3l | CentOS
Magento on LAMP CentOS7.2 64bits powered by IGS 1.0  | m-gw8b0o328tmvkdayxs5e | CentOS
LAMP CentOS 7.2 64bits powered by IGS 1.0            | m-gw8bvjaaebmebk1ovjbx | CentOS
RealSight APM V2.0  on CentOS 7.2 V2.0               | m-gw8bvjaaebmec1syw13z | CentOS
KASS Enterprise Content Management System 11.7.0     | m-gw8bvjaaebmeclja0kv4 | CentOS
Wowza Streaming Engine 4: BYOL Edition 4.6.0         | m-gw82wrqnfc7k1ar4vpz2 |
FlexGW  IPsec VPN on CentOS v2.5                     | m-gw82wrqnfc7k18s3rnzx | CentOS
LAMP on Ubuntu 14.04 64bits 1.0                      | m-gw8dq50o59ikcjf8nstp | Ubuntu
LNMP on Centos V1.1                                  | m-gw8g31s5d5j2s6dz2hha | CentOS
Tomcat + Nginx + My SQL Stack Package on Ubuntu v1.1 | m-gw8dq50o59ikctae82pb | Ubuntu
```

### One liner to get all ECS instance type in the configure region in your settings.

`aliyun ecs DescribeInstanceTypes --output cols=InstanceTypeId,CpuCoreCount,MemorySize`

### Result

```bash
InstanceTypeId             | CpuCoreCount | MemorySize
--------------             | ------------ | ----------
ecs.t1.xsmall              | 1            | 0.5
ecs.t1.small               | 1            | 1
ecs.s2.small               | 2            | 2
ecs.s3.medium              | 4            | 4
ecs.c1.small               | 8            | 8
ecs.c2.medium              | 16           | 16
ecs.s1.small               | 1            | 2
ecs.s2.large               | 2            | 4
ecs.s3.large               | 4            | 8
ecs.c1.large               | 8            | 16
ecs.c2.large               | 16           | 32
ecs.s1.medium              | 1            | 4
ecs.s2.xlarge              | 2            | 8
ecs.m1.medium              | 4            | 16
ecs.m1.xlarge              | 8            | 32
ecs.c2.xlarge              | 16           | 64
ecs.s1.large               | 1            | 8
ecs.s2.2xlarge             | 2            | 16
ecs.m2.medium              | 4            | 32
ecs.m2.xlarge              | 8            | 64
ecs.n1.tiny                | 1            | 1
ecs.n1.small               | 1            | 2
ecs.n1.medium              | 2            | 4
ecs.n1.large               | 4            | 8
ecs.n1.xlarge              | 8            | 16
ecs.n1.3xlarge             | 16           | 32
ecs.n1.7xlarge             | 32           | 64
ecs.n2.small               | 1            | 4
ecs.n2.medium              | 2            | 8
ecs.n2.large               | 4            | 16
ecs.n2.xlarge              | 8            | 32
ecs.n2.3xlarge             | 16           | 64
ecs.n2.7xlarge             | 32           | 128
ecs.e3.small               | 1            | 8
ecs.e3.medium              | 2            | 16
ecs.e3.large               | 4            | 32
ecs.e3.xlarge              | 8            | 64
ecs.e3.3xlarge             | 16           | 128
ecs.e3.7xlarge             | 32           | 256
ecs.sn1.medium             | 2            | 4
ecs.sn2.medium             | 2            | 8
ecs.sn1.large              | 4            | 8
ecs.sn1.xlarge             | 8            | 16
ecs.sn1.3xlarge            | 16           | 32
ecs.sn1.7xlarge            | 32           | 64
ecs.sn2.large              | 4            | 16
ecs.sn2.xlarge             | 8            | 32
ecs.sn2.3xlarge            | 16           | 64
ecs.sn2.7xlarge            | 32           | 128
ecs.n4.small               | 1            | 2
ecs.n4.large               | 2            | 4
ecs.n4.xlarge              | 4            | 8
ecs.n4.2xlarge             | 8            | 16
ecs.n4.4xlarge             | 16           | 32
ecs.n4.8xlarge             | 32           | 64
ecs.mn4.small              | 1            | 4
ecs.mn4.large              | 2            | 8
ecs.mn4.xlarge             | 4            | 16
ecs.mn4.2xlarge            | 8            | 32
ecs.mn4.4xlarge            | 16           | 64
ecs.mn4.8xlarge            | 32           | 128
ecs.xn4.small              | 1            | 1
ecs.e4.large               | 2            | 16
ecs.e4.xlarge              | 4            | 32
ecs.e4.2xlarge             | 8            | 64
ecs.e4.4xlarge             | 16           | 128
ecs.gn3.2xlarge            | 12           | 24
ecs.sn2.13xlarge           | 56           | 224
ecs.e4.small               | 1            | 8
ecs.se1.large              | 2            | 16
ecs.se1.xlarge             | 4            | 32
ecs.se1.2xlarge            | 8            | 64
ecs.se1.4xlarge            | 16           | 128
ecs.se1.8xlarge            | 32           | 256
ecs.se1.14xlarge           | 56           | 480
ecs.ga1.4xlarge            | 16           | 40
ecs.ga1.8xlarge            | 32           | 80
ecs.ga1.14xlarge           | 56           | 160
ecs.gn4.8xlarge            | 32           | 48
ecs.gn4.14xlarge           | 56           | 96
ecs.i1.xlarge              | 4            | 16
ecs.i1.2xlarge             | 8            | 32
ecs.i1.4xlarge             | 16           | 64
ecs.i1.8xlarge             | 32           | 128
ecs.i1.14xlarge            | 56           | 224
ecs.cm4.xlarge             | 4            | 16
ecs.cm4.2xlarge            | 8            | 32
ecs.cm4.4xlarge            | 16           | 64
ecs.ce4.xlarge             | 4            | 32
ecs.c4.xlarge              | 4            | 8
ecs.c4.2xlarge             | 8            | 16
ecs.c4.4xlarge             | 16           | 32
ecs.cm4.6xlarge            | 24           | 96
ecs.sc1.4xlarge            | 16           | 16
ecs.d1.2xlarge             | 8            | 32
ecs.d1.4xlarge             | 16           | 64
ecs.d1.6xlarge             | 24           | 96
ecs.d1.8xlarge             | 32           | 128
ecs.d1.14xlarge            | 56           | 224
ecs.ga1.2xlarge            | 8            | 20
ecs.ga1.xlarge             | 4            | 10
ecs.sn1ne.large            | 2            | 4
ecs.sn1ne.xlarge           | 4            | 8
ecs.sn1ne.2xlarge          | 8            | 16
ecs.sn1ne.4xlarge          | 16           | 32
ecs.sn1ne.8xlarge          | 32           | 64
ecs.sn2ne.large            | 2            | 8
ecs.sn2ne.xlarge           | 4            | 16
ecs.sn2ne.2xlarge          | 8            | 32
ecs.sn2ne.4xlarge          | 16           | 64
ecs.sn2ne.8xlarge          | 32           | 128
ecs.sn2ne.14xlarge         | 56           | 224
ecs.se1ne.large            | 2            | 16
ecs.se1ne.xlarge           | 4            | 32
ecs.se1ne.2xlarge          | 8            | 64
ecs.se1ne.4xlarge          | 16           | 128
ecs.se1ne.8xlarge          | 32           | 256
ecs.se1ne.14xlarge         | 56           | 480
ecs.i1-c10d1.8xlarge       | 32           | 128
ecs.i1-c5d1.4xlarge        | 16           | 64
ecs.f1-c8f1.2xlarge        | 8            | 60
ecs.f1-c8f1.4xlarge        | 16           | 120
ecs.gn5-c4g1.xlarge        | 4            | 30
ecs.gn5-c8g1.2xlarge       | 8            | 60
ecs.gn5-c4g1.2xlarge       | 8            | 60
ecs.gn5-c8g1.4xlarge       | 16           | 120
ecs.gn5-c8g1.8xlarge       | 32           | 240
ecs.gn5-c8g1.14xlarge      | 54           | 480
ecs.gn4-c4g1.xlarge        | 4            | 30
ecs.gn4-c8g1.2xlarge       | 8            | 30
ecs.gn4-c4g1.2xlarge       | 8            | 60
ecs.gn4-c8g1.4xlarge       | 16           | 60
ecs.d1ne.2xlarge           | 8            | 32
ecs.d1ne.4xlarge           | 16           | 64
ecs.d1ne.6xlarge           | 24           | 96
ecs.d1ne.8xlarge           | 32           | 128
ecs.d1ne.14xlarge          | 56           | 224
ecs.d1-c8d3.8xlarge        | 32           | 128
ecs.d1-c14d3.14xlarge      | 56           | 160
ecs.c5.large               | 2            | 4
ecs.c5.xlarge              | 4            | 8
ecs.c5.2xlarge             | 8            | 16
ecs.c5.4xlarge             | 16           | 32
ecs.c5.6xlarge             | 24           | 48
ecs.c5.8xlarge             | 32           | 64
ecs.c5.16xlarge            | 64           | 128
ecs.g5.large               | 2            | 8
ecs.g5.xlarge              | 4            | 16
ecs.g5.2xlarge             | 8            | 32
ecs.g5.4xlarge             | 16           | 64
ecs.g5.6xlarge             | 24           | 96
ecs.g5.8xlarge             | 32           | 128
ecs.g5.16xlarge            | 64           | 256
ecs.r5.large               | 2            | 16
ecs.r5.xlarge              | 4            | 32
ecs.r5.2xlarge             | 8            | 64
ecs.r5.4xlarge             | 16           | 128
ecs.r5.6xlarge             | 24           | 192
ecs.r5.8xlarge             | 32           | 256
ecs.r5.16xlarge            | 64           | 512
ecs.r5.22xlarge            | 88           | 704
ecs.hfc5.large             | 2            | 4
ecs.hfc5.xlarge            | 4            | 8
ecs.hfc5.2xlarge           | 8            | 16
ecs.hfc5.4xlarge           | 16           | 32
ecs.hfc5.6xlarge           | 24           | 48
ecs.hfc5.8xlarge           | 32           | 64
ecs.hfg5.large             | 2            | 8
ecs.hfg5.xlarge            | 4            | 16
ecs.hfg5.2xlarge           | 8            | 32
ecs.hfg5.4xlarge           | 16           | 64
ecs.hfg5.6xlarge           | 24           | 96
ecs.hfg5.8xlarge           | 32           | 128
ecs.hfg5.14xlarge          | 56           | 160
ecs.i2.xlarge              | 4            | 32
ecs.i2.2xlarge             | 8            | 64
ecs.i2.4xlarge             | 16           | 128
ecs.i2.8xlarge             | 32           | 256
ecs.i2.16xlarge            | 64           | 512
ecs.gn5-c28g1.7xlarge      | 28           | 112
ecs.gn5-c28g1.14xlarge     | 56           | 224
ecs.re4.20xlarge           | 80           | 960
ecs.re4.40xlarge           | 160          | 1920
ecs.gn5i-c2g1.large        | 2            | 8
ecs.gn5i-c4g1.xlarge       | 4            | 16
ecs.gn5i-c8g1.2xlarge      | 8            | 32
ecs.gn5i-c16g1.4xlarge     | 16           | 64
ecs.gn5i-c28g1.14xlarge    | 56           | 224
ecs.gn5t.7xlarge           | 28           | 112
ecs.gn5t.14xlarge          | 56           | 224
ecs.t5-c1m1.large          | 2            | 2
ecs.t5-c1m1.xlarge         | 4            | 4
ecs.t5-c1m1.2xlarge        | 8            | 8
ecs.t5-c1m1.4xlarge        | 16           | 16
ecs.t5-c1m2.large          | 2            | 4
ecs.t5-c1m2.xlarge         | 4            | 8
ecs.t5-c1m2.2xlarge        | 8            | 16
ecs.t5-c1m2.4xlarge        | 16           | 32
ecs.t5-c1m4.large          | 2            | 8
ecs.t5-c1m4.xlarge         | 4            | 16
ecs.t5-c1m4.2xlarge        | 8            | 32
ecs.t5-lc2m1.nano          | 1            | 0.5
ecs.t5-lc1m1.small         | 1            | 1
ecs.t5-lc1m2.small         | 1            | 2
ecs.t5-lc1m2.large         | 2            | 4
ecs.t5-lc1m4.large         | 2            | 8
ecs.f1-c28f1.7xlarge       | 28           | 112
ecs.f1-c28f1.14xlarge      | 56           | 224
ecs.sccg5.24xlarge         | 96           | 384
ecs.scch5.16xlarge         | 64           | 192
ecs.sccgn5d.16xlarge       | 64           | 256
ecs.sccgn5.16xlarge        | 64           | 512
ecs.ebmg5.24xlarge         | 96           | 384
ecs.ebmr5.24xlarge         | 96           | 768
ecs.f2-c8f1.2xlarge        | 8            | 60
ecs.f2-c28f1.7xlarge       | 28           | 112
ecs.f2-c8f1.4xlarge        | 16           | 120
ecs.f2-c28f1.14xlarge      | 56           | 224
ecs.gn5i-c40g1.10xlarge    | 40           | 160
ecs.gn5i-c48g1.12xlarge    | 48           | 192
ecs.ebmr5.2xlarge          | 8            | 64
ecs.ebmr4.4xlarge          | 16           | 128
ecs.ebmg4.8xlarge          | 32           | 128
ecs.ebmg4.16xlarge         | 64           | 256
ecs.ebma1.24xlarge         | 96           | 256
ecs.gn6p-c8g1.4xlarge      | 16           | 64
ecs.gn5i-c16g1.8xlarge     | 32           | 128
ecs.sn1ne.3xlarge          | 12           | 24
ecs.sn1ne.6xlarge          | 24           | 48
ecs.sn2ne.3xlarge          | 12           | 48
ecs.sn2ne.6xlarge          | 24           | 96
ecs.se1ne.3xlarge          | 12           | 96
ecs.se1ne.6xlarge          | 24           | 192
ecs.c4.3xlarge             | 12           | 24
ecs.cm4.3xlarge            | 12           | 48
ecs.ce4.2xlarge            | 8            | 64
ecs.c5.3xlarge             | 12           | 24
ecs.hfc5.3xlarge           | 12           | 24
ecs.g5.3xlarge             | 12           | 48
ecs.g5.22xlarge            | 88           | 352
ecs.hfg5.3xlarge           | 12           | 48
ecs.r5.3xlarge             | 12           | 96
ecs.i1.3xlarge             | 12           | 48
ecs.i1.6xlarge             | 24           | 96
ecs.d1.3xlarge             | 12           | 48
ecs.g5se.large             | 2            | 8
ecs.g5se.xlarge            | 4            | 16
ecs.g5se.2xlarge           | 8            | 32
ecs.g5se.4xlarge           | 16           | 64
ecs.g5se.6xlarge           | 24           | 96
ecs.g5se.8xlarge           | 32           | 128
ecs.g5se.16xlarge          | 64           | 256
ecs.g5se.18xlarge          | 70           | 336
ecs.gn5i-c12g1.6xlarge     | 24           | 96
ecs.gn5t.4xlarge           | 16           | 56
ecs.ebmgn5t.16xlarge       | 64           | 512
ecs.sccgn5t.16xlarge       | 64           | 512
ecs.sccgn6.24xlarge        | 96           | 512
ecs.ebmgn5.16xlarge        | 64           | 256
ecs.ebmhfg5.2xlarge        | 8            | 32
ecs.ebmhfg4.4xlarge        | 16           | 64
ecs.ebmc4.8xlarge          | 32           | 64
ecs.ic5.large              | 2            | 2
ecs.ic5.xlarge             | 4            | 4
ecs.ic5.2xlarge            | 8            | 8
ecs.ic5.3xlarge            | 12           | 12
ecs.ic5.4xlarge            | 16           | 16
ecs.ic5.6xlarge            | 24           | 24
ecs.ic5.8xlarge            | 32           | 32
ecs.ic5.16xlarge           | 64           | 64
ecs.gn5d-c8g1.8xlarge      | 32           | 224
ecs.gn5-c48g1.12xlarge     | 48           | 164
ecs.ebmgn5i.24xlarge       | 96           | 384
ecs.ebmi2.24xlarge         | 96           | 768
ecs.d1ne-c8d3.8xlarge      | 32           | 128
ecs.d1ne-c14d3.14xlarge    | 56           | 160
ecs.c5-618.22xlarge        | 88           | 160
ecs.g5-618.22xlarge        | 88           | 344
ecs.f3-c4f1.xlarge         | 4            | 16
ecs.f3-c8f1.2xlarge        | 8            | 32
ecs.f3-c12f1.3xlarge       | 12           | 48
ecs.f3-c16f1.4xlarge       | 16           | 64
ecs.f3-c24f1.6xlarge       | 24           | 96
ecs.f3-c32f1.8xlarge       | 32           | 128
ecs.f3-c40f1.10xlarge      | 40           | 160
ecs.f3-c6f1.3xlarge        | 12           | 48
ecs.f3-c8f1.4xlarge        | 16           | 64
ecs.f3-c12f1.6xlarge       | 24           | 96
ecs.f3-c16f1.8xlarge       | 32           | 128
ecs.f3-c32f1.16xlarge      | 64           | 256
ecs.f3-c8f1.8xarge         | 32           | 128
ecs.f3-c16f1.16xlarge      | 64           | 256
ecs.ebmgn5t.10xlarge       | 40           | 256
ecs.gn6v-c8g1.2xlarge      | 8            | 32
ecs.gn6v-c8g1.4xlarge      | 16           | 64
ecs.gn6v-c8g1.8xlarge      | 32           | 128
ecs.gn6v-c8g1.16xlarge     | 64           | 256
ecs.g5-618.21xlarge        | 84           | 344
ecs.c5-618e.22xlarge       | 88           | 160
ecs.g5-618e.22xlarge       | 88           | 344
ecs.g5-618e.21xlarge       | 84           | 344
ecs.ebmi3.24xlarge         | 96           | 384
ecs.re5.15xlarge           | 60           | 990
ecs.re5.30xlarge           | 120          | 1980
ecs.re5.45xlarge           | 180          | 2970
ecs.g5-618e.16xlarge       | 64           | 256
ecs.g5-618e.6xlarge        | 24           | 88
ecs.i2g.2xlarge            | 8            | 32
ecs.i2g.4xlarge            | 16           | 64
ecs.i2g.8xlarge            | 32           | 128
ecs.i2g.16xlarge           | 64           | 256
ecs.r1.7xlarge             | 28           | 104
ecs.c5.22xlarge            | 88           | 160
ecs.d1ne-8tc14d3.14xlarge  | 56           | 160
ecs.re4e.40xlarge          | 160          | 3840
ecs.d1ne-c14d3g.14xlarge   | 56           | 224
ecs.d1ne-8tc14d3g.14xlarge | 56           | 160
ecs.ebmg5s.24xlarge        | 96           | 384
ecs.sn1ne.22xlarge         | 88           | 160
ecs.sn2ne.22xlarge         | 88           | 352
ecs.se1ne.22xlarge         | 88           | 704
```

### One liner to get list of instances with name, CPU, Memory, OS Name and Status
`aliyun ecs DescribeInstances --output cols=ZoneId,InstanceName,Cpu,Memory,OsName,InstanceId`

### Result

```bash
ZoneId        | InstanceName     | Cpu | Memory | OsName | InstanceId
------        | ------------     | --- | ------ | ------ | ----------
eu-central-1a | terraform        | 2   | 4096   | <nil>  | i-gwxxxxxxxxxxxxxxxxxx
eu-central-1a | def-vpc-sharing  | 2   | 2048   | <nil>  | i-gwxxxxxxxxxxxxxxxxxx
eu-central-1a | def-vpc-zabbix   | 2   | 4096   | <nil>  | i-gwxxxxxxxxxxxxxxxxxx
eu-central-1b | def-vpc-ansible  | 1   | 1024   | <nil>  | i-gwxxxxxxxxxxxxxxxxxx
eu-central-1a | def-vpc-vmw      | 1   | 2048   | <nil>  | i-gwxxxxxxxxxxxxxxxxxx
eu-central-1a | def-vpc-rt       | 2   | 4096   | <nil>  | i-gwxxxxxxxxxxxxxxxxxx
eu-central-1a | def-vpc-jumphost | 1   | 1024   | <nil>  | i-gwxxxxxxxxxxxxxxxxxx
```

### One line to start ECS instance from command line

`aliyun ecs StartInstance --InstanceId i-gwxxxxxxxxxxxxxxxxxx`

```bash
{"RequestId":"BAAC6C61-C207-4DE6-A976-XXXXXXXXX"}
```

### One liner to get list of instances with Hostname and Network Interfaces
`aliyun ecs DescribeInstances --RegionId eu-central-1 --output cols=HostName,NetworkInterfaces`

### Result

```bash
HostName                | NetworkInterfaces
--------                | -----------------
webserver002            | map[NetworkInterface:[map[MacAddress:00:16:3e:00:1b:04 PrimaryIpAddress:192.168.0.187 NetworkInterfaceId:eni-gw828kgsr9n4hjolv3pz]]]
webserver001            | map[NetworkInterface:[map[MacAddress:00:16:3e:00:0a:37 PrimaryIpAddress:192.168.0.188 NetworkInterfaceId:eni-gw828kgsr9n4hjolv3py]]]
webserver               | map[NetworkInterface:[map[MacAddress:00:16:3e:00:03:35 PrimaryIpAddress:192.168.0.170 NetworkInterfaceId:eni-gw84zq5fnih3qi37s2xu]]]
webserver               | map[NetworkInterface:[map[MacAddress:00:16:3e:00:19:eb PrimaryIpAddress:192.168.0.168 NetworkInterfaceId:eni-gw8blruqz22mt8xzggw0]]]
chmurowisko2            | map[NetworkInterface:[map[MacAddress:00:16:3e:01:76:12 PrimaryIpAddress:192.168.0.164 NetworkInterfaceId:eni-gw841i7u48pfqe3ezt84]]]
chmurowisko             | map[NetworkInterface:[map[MacAddress:00:16:3e:01:79:be PrimaryIpAddress:192.168.0.163 NetworkInterfaceId:eni-gw841i7u48pfpog0j3ip]]]
terraform               | map[NetworkInterface:[map[MacAddress:00:16:3e:01:6a:3e PrimaryIpAddress:172.25.18.46 NetworkInterfaceId:eni-gw8f9mvfddriihb0ye0c]]]
sharing                 | map[NetworkInterface:[map[MacAddress:00:16:3e:01:28:f9 PrimaryIpAddress:172.25.18.35 NetworkInterfaceId:eni-gw89je7fi75h453d03jr]]]
zabbix                  | map[NetworkInterface:[map[NetworkInterfaceId:eni-gw8acanqm4y46sao3lvq MacAddress:00:16:3e:01:22:c2 PrimaryIpAddress:172.25.18.31]]]
iZgw8iej0t1njrejjajoyyZ | map[NetworkInterface:[map[MacAddress:00:16:3e:01:20:47 PrimaryIpAddress:172.25.62.57 NetworkInterfaceId:eni-gw8iej0t1njrejjhkwot]]]
```
