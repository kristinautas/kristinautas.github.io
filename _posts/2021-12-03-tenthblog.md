---
layout: post
title: "Blog 10  - Back up solutions in Linux. Part 2"
date: 2021-11-19 14:21:28 -0700
categories: ubuntu blog
---
<b>Using Relax-and-Recover (ReaR)</b>
ReaR is a powerful disaster recovery and system migration tool written in Bash. It can also be <br>installed on Ubuntu using. The following command: <br>
`sudo apt install rear`<br>
Once the packages have been installed, check out the main configuration file <br>called /etc/rear/local.conf that contains all the configuration options. By default, ReaR <br>makes ISO files, but it also supports Samba (CIFS), USB, and NFS as destinations. <br>
<b>Backing up to a local NFS server using ReaR</b><br>
Let’s take a look at the example of backing up to an NFS server. Let’s say, we already have an <b>NFS server set up on one of our Ubuntu machines on our network.<b>
First, we must configure the NFS server. The configuration file for NFS /etc/exports stores <b>information about the share's location. Before we add any new information about the ReaR <b>backup share's location, we will create a new directory for our RearR backups as follows:<b>
`sudo mkdir /home/export/rear `
Now, we need to change ownership because we will not have permission to write the backup to <br>this location of the owner is root:<br>
`sudo chown -R nobody:nogroup /home/export/rear/`<br>
Now, open the `/etc/exports` file and add a new line for the backup directory as follows:<br>
`/home/export/rear	192.168.0.0/24(rw,sync,no_subtree_check) `
Then, restart the NFS service and run the `exportfs -s` command. <br>
Now, go back to the local machine and edit the ReaR configuration file to use the backup server. Edit the `/etc/rear/local.conf` file and add the lines shown in the following output. Make sure to use your own system's IP address:<br>
OUTPUT=ISO <br>
OUPUT_URL=nfs://192.168.0.244/home/export/rear/ <br>
BACKUP=NETFS <br>
BACKUP_URL=nfs://192.168.0.244/home/export/rear <br>
The lines shown here represent the following: <br>
•	OUTPUT: The bootable image type, which in our case is ISO <br>
•	OUTPUT_URL: The backup target <br>
•	BACKUP : The backup method used <br>
•	BACKUP_URL: The backup target's location <br>
Now, run the `mkbackup  -v  -d` command: <br>
`sudo rear -v -d mkbackup`<br>
Once it has finished, you can check the NFS directory to view its output using ls -la <br>
Once the backup has been written on the NFS server, you will be able to restore the system by  <br> using a USB disk or DVD with the ISO image that was written on the NFS server. <br>
<b>Backing up to USB using ReaR </b><br>
You can also directly back up on the USB disk. After inserting disk into the USB port, format it <br> by using the `rear format /dev/sdb `command. <br>
Then, modify the `/etc/rear/local.conf` file so that it uses the USB as the backup destination. <br>These new lines should look as follows:<br>
OURPUT=USB <br>
BACKUP=NETFS <br>
BACKUP_URL=”usb:///dev/disk/by-label/REAR-000” <br>

Run the following command:<br>
`rear -v mkbackup`<br>

Once it has finished, you will find the ISO and the `tar.gz` files on the USB drive. <br>
To recover the system, you will need to boot from the USB drive and select the option, that  <br>says `Recover "hostname"`, which is the hostname of the computer you backed up.<br>
Knowing how to do system backup and recovery can save the company, the client's data, time, <br>and money. Strong diagnostics toolset and troubleshooting knowledge will always come in <br>handy for every system administrator. In the next blog post, I will show you some of the <br>best diagnostic tools in Linux. <br>


