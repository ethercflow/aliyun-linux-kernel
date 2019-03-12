Aliyun Linux OS - An open-source Linux distribution powered by Alibaba Cloud
============================================================================

Table of Contents
-----------------
1. [What is Aliyun Linux OS](#1-what-is-aliyun-linux-os)
2. [How to use](#2-how-to-use)
3. [Getting source](#3-getting-source)
4. [Getting helps](#4-getting-helps)

-------------------------

## 1. What is Aliyun Linux OS

Aliyun Linux OS is an open-source Linux distribution originated by Alibaba Operating System team, aiming to deliver OS services with various functionality, high performance and stability to Alibaba Cloud Elastic Compute Service (ECS) customers.

Current released version is Aliyun Linux OS version 2, or known as 'Aliyun Linux 2'.

## 2. How to use

Simply buy an ECS instance and getting started: [chs](https://ecs-buy.aliyun.com/), [eng](https://ecs-buy-intl.aliyun.com/).

## 3. Getting source

Inside an Aliyun Linux 2 OS, you should be able to fetch source RPMs via `yumdownloader` tool (make sure you have `yum-utils` package installed first):

```bash
sudo yum install -y yum-utils
sudo yumdownloader --source <source package>
```

## 4. Getting Helps

To get helps when using Aliyun Linux OS, you can
+ File a [ticket](https://selfservice.console.aliyun.com/ticket/createIndex) if you are an Alibaba Cloud ECS customer; or
+ Send us an E-mail to [alicloud-linux-os@service.alibaba.com](mailto:alicloud-linux-os@service.alibaba.com).
