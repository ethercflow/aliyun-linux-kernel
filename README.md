Aliyun (Alibaba Cloud) Linux Kernel Git Tree
============================================

Table of Contents
-----------------
1. [What is Aliyun Linux Kernel](#1-what-is-aliyun-linux-kernel)
2. [Getting Started](#2-getting-started)
   1. [Run with pre-built RPMs (recommended)](#21-run-with-pre-built-rpms-recommended)
   2. [Compile from source](#22-compile-from-source)
3. [Contributing](#3-contributing)
4. [Credits](#4-credits)
5. [License](#5-license)
6. [Contact Us](#6-contact-us)

---------------------------------


## 1. What is Aliyun Linux Kernel

Aliyun Linux Kernel (ALK), a customized and optimized version of Linux kernel, is originated by Alibaba Operating System Team (formerly known as Taobao Kernel Team). ALK is installed as the default kernel in Aliyun Linux OS version 2 (a.k.a Aliyun Linux 2), which is running on Alibaba Cloud Elastic Compute Service (ECS) product. In ALK, several features and enhancements apdated to specific Alibaba Cloud infrastructre and products have been made to help Alibaba Cloud customers to achieve better user experiences.

Like many other kernels, ALK should work with almost all commonly-used Linux distributions, however, we highly recommend you run it in Aliyun Linux OS with Alibaba Cloud ECS instances to get best functionality, performance and stablity.

To get more information about Aliyun Linux OS, please refer to [this](os/README.md) link.

## 2. Getting Started

To use ALK, you may want either to run a pre-built version or to compile it from source codes. Note that the default kernel configuration file is a customized version for Alibaba Cloud ECS instances, you might need to enable specific drivers and re-compile the kernel if you want to run it on non-ECS platforms. If unsure.

### 2.1 Run with pre-built RPMs (recommended)

Install from YUM source is the most recommended way:

+ (a) Create a new YUM repo file:

```bash
sudo vim /etc/yum.repos.d/aliyun-2.1903-plus.repo
```

+ (b) Fill repository information into the repo file:

```bash
[plus]
name=Aliyun Linux 2.1903 Plus Software Collections
baseurl=http://mirrors.aliyun.com/alinux/2.1903/plus/x86_64/
enabled=1
gpgcheck=1
gpgkey=http://mirrors.aliyun.com/alinux/RPM-GPG-KEY-ALIYUN
```

+ (c) Install the kernel:

```bash
sudo yum install -y kernel kernel-devel kernel-headers
```

+ (d) Reboot system and enjoy the new ALK.

### 2.2 Compile from source

+ (a) Fetch kernel source either
  + from [Releases page](https://github.com/alibaba/aliyun-linux-kernel/releases) for a stable release, then extract the tar ball, or
  + cloning from [github repo](https://github.com/alibaba/aliyun-linux-kernel) and switching to latest dev branch. Note that dev branch changes time to time, to find out the most recent one, see [LATEST_BRANCH](LATEST_BRANCH) file.
+ (b) Fetch a [default kernel config](config-4.19.y-x86_64) from master branch and rename it to `.config`, then save it to the top of kernel source directory;
+ (c) Compile and install kernel via the following commands:

```bash
make oldconfig
make -jN # N normally refers to the CPU core numbers on the system
make modules -jN
sudo make modules_install
sudo make install
```

+ (4) Reboot system.

## 3. Contributing

There are different ways to contribute to ALK project, please read [CONTRIBUTING](CONTRIBUTING.md) file to get more details.

## 4. Credits

A full list of contributors from teams and individuals inside and out of Alibaba Group could be found in [CREDITS](CREDITS) file. And special thanks would be given to:
+ [CentOS project](https://www.centos.org/);
+ [Clear Linux project](https://clearlinux.org/);
+ [Intel 0-Day (LKP) project](https://01.org/lkp);
+ [Linux kernel project](https://www.kernel.org/).

## 5. License

We use the same license as the upstream does, so please refer to the COPYING file in each branch of kernel source tree.

## 6. Contact Us

+ File a [ticket](https://selfservice.console.aliyun.com/ticket/createIndex) if you are an Alibaba Cloud ECS customer;
+ Send us an E-mail to [alicloud-linux-os@service.alibaba.com](mailto:alicloud-linux-os@service.alibaba.com) is always a good idea.
