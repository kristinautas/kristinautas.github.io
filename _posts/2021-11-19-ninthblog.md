---
layout: post
title: "Blog 9  - Back up solutions in Linux"
date: 2021-11-19 14:21:28 -0700
categories: ubuntu blog
---
It is extremely important to back up your data. Unfortunately, many people start considering<br> backup solutions only after the disaster has already happened. I suggest we take a proactive <br>approach to this matter and learn how to perform backups before data loss occurs. There’re <br>many backup types and methods. Today, we are going to talk about disk cloning solutions, <br>such as`dd` command, the `ddrescue`command, and the `Relax-and-Recover (ReaR) `software tool.<br><br>
 <b>The `dd` command</b><br><br>
The `dd` command is the most popular linux back up command. It is used to copy an entire disk, block by block, from a source to a destination. It is important to check that there is enough space on the destination disk to fit data from the source. By running `fdisk -l` command we can check both source and destination disk space. Using the `dd` command, we will need to make sure that the source file will fit into the destination. <br><br>
Once we know we have enough disk space, we can proceed with the cloning. Let’s say we want to clone `/dev/sda` to `/dev/sdb`. In order to do that, run the following command: <br>
`sudo dd if=if=/dev/sda of=/dev/sdb conv=noerror, sync status=progress` <br>

•	if=/dev/sda represents the input file. <br>
•	of=/dev/sdb represents the output file.<br>
•	conv=noerror represents the instruction to ignore errors.<br>
•	sync represents the instruction to pad each block with nulls in case if full block can’t be read due to erorr. <br>
•	status=progress shows statistics about the transfer process.<br><br>

<b>The `ddrescue` command</b><br>
Using the `ddrescue` command is another way to clone your disk. At first, this command will try <br>to copy only the healthy parts for the first time. To copy good parts and map the errors to a <br>destination file, you need to use `ddrescue` twice. To install this command on Ubuntu, run <br>the following apt command:<br>
`sudo apt install gddrescue`<br>
Now, use ddrescue to clone the disk. Run:<br>
`sudo ddrescue -n /dev/sda /dev/sdb rescue.map --force` 

--force option is used to make sure that everything on the destination will be overwritten. <br><br>

The <b>Relax-and-Recover (ReaR)</b> software tool is a little more complicated in use, we will cover it our future blog posts. Stay tuned.

