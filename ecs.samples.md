# ECS

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

### One liner to get all ECS instance type in the configure region in your settings.

`aliyun ecs DescribeInstanceTypes --output cols=InstanceTypeId,CpuCoreCount,MemorySize`
