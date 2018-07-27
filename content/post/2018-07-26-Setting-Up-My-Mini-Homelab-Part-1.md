---
title: "Setting Up My Mini Home Lab Part 1"
date: 2018-07-26T20:40:36-04:00
draft: false
tags: ["VMware","vSphere67","Home Lab","2018"]
---

Recently, it had become abundantly clear that I needed a home lab.
I have seen some amazing home lab builds around the internet and am in awe of most of them.
Multiple physical hosts, physical switches, external storage, and in some cases complete HCI setups.
This is what I wanted.
This is what I needed!
However, I am extraordinarily cheap, and spending that kind of money on a lab might give me a heart attack and if I survived that my wife might kill me anyways!

<!--more -->

I decided that I should start small and move towards building something bigger and badder once I can demonstrate to myself the value in the cash that I would be spending.
My needs are not extreme.
I just need to be able to play with a few different versions of VMware, be able to test out PowerCLI and Zerto scripts, and play around with other virtualization technologies as I come across them.
Based on my limited needs, I decided to run nested virtualization on my primary desktop.

Before I started my desktop only had 16 GB RAM 1 x 1 TB SSD and 1 x 3 TB HDD running Windows 10 Pro and running the imbedded Hyper-V platform.
It is able to address up to 64 GB RAM and had 4 open SATA ports.
To get the needed memory and storage capacity I purchased 64 GB DDR4 RAM to replace my existing 2 x 8 GB chips and an additional 1 TB SSD and 4 TB HDD for plenty of storage.
I also uninstalled Hyper-V and rebuilt my running VMs into VMware Workstation 14.

At this point, I was setup to begin configuring VMware Workstation for my various host networks as well as building the nested VMware vSphere 6.7 ESXi hosts.
In the end, I will be able to run a 3-host cluster with "external" storage support without having to invest in a ton of extra hardware.
An extra benefit is that these systems can be paused and resumed almost on demand.
This allows me to quickly free up resources when I do not need them, but quickly resume when I want to test.
In my next post, I will detail my VMware workstation setup along with how I decided to build my first lab.

Thoughts or comments?
Please feel free to leave them below!