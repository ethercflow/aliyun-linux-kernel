Contributing to Aliyun Linux Kernel
===================================

Table of Contents
-----------------
1. [Reporting bugs](#1-reporting-bugs)
  1. [Reporting security issues](#11-reporting-security-issues)
  2. [Reporting crash issues](#12-reporting-crash-issues)
  3. [Reporting general issues](#13-reporting-general-issues)
  4. [Reporting Aliyun Linux OS issues](#14-reporting-aliyun-linux-os-issues)
2. [Comming up with patches](#2-coming-up-with-patches)

-----------------

## 1. Reporting Bugs

The easiest way to participate in contributing to the project is just use ALK and Aliyun Linux OS, then report bugs to us. However, there are some ground rules against special types of bugs when file a bug.

### 1.1 Reporting security issues

We welcome reports from security researchers and experts about possible security vulnerabilities with our kernel and operating system, however we discourage anyone to spread security issue details. To report a security issue, please send a private email to [alicloud-linux-os@service.alibaba.com](mailto:alibaba-linux-os@service.alibaba.com), we do appreciate it and will review it carefully at one.

### 1.2 Reporting crash issues

Kernel panic and system crash is critical to any users, we would raise priority against such bug reports, Please file bug reports in our [project issues page](https://github.com/alibaba/aliyun-linux-kernel/issues), in order to get better understanding of your problem, please include the following information as much as possible:

+ Kdump core or kernel stack trace when crashed;
+ Suspicious applications or operations that trigger the crash;
+ Kernel version if kdump core or full kernel stack trace not provided.

Digging into a crash issue is always a difficult thing, we do thank to anyone who is willing to help with reproducing the crashes.

### 1.3 Reporting general issues

Feel free to file bug reports in our [project issues page](https://github.com/alibaba/aliyun-linux-kernel/issues)

### 1.4 Reporting Aliyun Linux OS issues

ALK has tight connections with Aliyun Linux OS, if you run into any Aliyun Linux OS problems, feel free to file a bug report in [project issues page](https://github.com/alibaba/aliyun-linux-kernel/issues) as well, or start a thread in [Alibaba Cloud Developer forum](https://bbs.aliyun.com/fourms.php).

## 2. Coming up with patches

You can follow the [submitting patches guide from kernel.org](https://www.kernel.org/doc/html/latest/process/submitting-patches.html), when your code is ready, you can just send a [pull request](https://github.com/alibaba/aliyun-linux-kernel/pulls) to us.
