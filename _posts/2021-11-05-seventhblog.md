---
layout: post
title: "Blog 7 - Anatomy of a Disk"
date: 2021-11-05 14:21:28 -0700
categories: ubuntu blog
---
Did you know you can create multiple filesystems on the same disk? It's called <b>partitioning</b>. <br>
In Linux, the whole partition is represented as `/dev/sda`. `/dev/sda1` is the<br> first partition, `/dev/sda2` is the second etc. If you need to separate your<br> data, it is much more efficient to create a partition instead of using the<br> entire disk for one filesystem.<br>
If you want to find out how many partitions there are on the disk and information <br> about them, you need to look at the <b>Partition Table</b>. This table
has information about the beginning and the end of the partitions, what sectors of the disk belong to which partition, if there are bootable partitions, etc. <br>
There are two main types of partition tables used: <b>MBR</b> and <b>GIUD</b>.<br>
They have some differences like <b>MBR</b> can have primary, extended and logical<br> partitions, while <b>GPT</b> has only one type of partition, but it's <br>
possible to make many of them. There're more differences, but they are outside<br> of the scope of this blog post.<br>
If you want to take a look at your partitioning table, you can run `sudo parted -l`.<br> This command will show you primary, logical and etendedpartitions on your computer. <br>
Below is the output of this command in case of <b>MBR</b> partitioning table. <br>
`pete@icebox:~$ sudo parted -l

Model: Seagate (scsi)<br>

Disk /dev/sda: 21.5GBp<br>

Sector size (logical/physical): 512B/512B<br>

Partition Table: msdos<br>


Number  Start   End     Size    Type      File system     Flags<br>

 1      1049kB  6860MB  6859MB  primary   ext4            boot<br>

 2      6861MB  21.5GB  14.6GB  extended<br>

 5      6861MB  7380MB  519MB   logical   linux-swap(v1)<br>

 6      7381MB  21.5GB  14.1GB  logical   xfs`<br>

There are a lot of tools that you can use to partition your disk. You will find<br> some of them listed below:<br>
•	<b>fdisk</b> - basic command-line partitioning tool that doesn't support GPT<br>
•	<b>parted</b> - command-line tool that supports MBR and GPT<br>
•	<b>gparted</b> - this is the GUI version of parted<br>
•	<b>gdisk</b> - fdisk, but it does not support MBR only GPT<br>


