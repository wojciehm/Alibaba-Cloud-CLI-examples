# ECS

## One liner to get all images ID sorted out by OS Name, Platorm, OS Type, Architecture and ImageID

aliyun ecs DescribeImages --RegionId eu-central-1 --ImageOwnerAlias system --output cols=ImageName,ImageId,Platform

## One liner to get images from Alibaba Cloud Marketplace

aliyun ecs DescribeImages --RegionId eu-central-1 --ImageOwnerAlias marketplace --output cols=ImageName,ImageId,Platform

## One liner to get all ECS instance type in the configure region in your settings.

aliyun ecs DescribeInstanceTypes --output cols=InstanceTypeId,CpuCoreCount,MemorySize
