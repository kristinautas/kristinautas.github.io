---
layout: post
title: "Blog 9  - Back up solutions in Linux"
date: 2021-11-19 14:21:28 -0700
categories: ubuntu blog
---
<b>Using Relax-and-Recover (ReaR)</b>
ReaR is a powerful disaster recovery and system migration tool written in Bash. It can also be <br>installed on Ubuntu using. The following command: <br>
`sudo apt install rear`<br>
Once the packages have been installed, check out the main configuration file <br>called /etc/rear/local.conf that contains all the configuration options. By default, ReaR <br>makes ISO files, but it also supports Samba (CIFS), USB, and NFS as destinations. <br>
<b>Backing up to a local NFS server using ReaR<b>
Let’s take a look at the example of backing up to an NFS server. Let’s say, we already have an <b>NFS server set up on one of our Ubuntu machines on our network.<b>
First, we must configure the NFS server. The configuration file for NFS /etc/exports stores <b>information about the share's location. Before we add any new information about the ReaR <b>backup share's location, we will create a new directory for our RearR backups as follows:<b>
`sudo mkdir /home/export/rear `
Now, we need to change ownership because we will not have permission to write the backup to <br>this location of the owner is root:<br>
`sudo chown -R nobody:nogroup /home/export/rear/`<br>
Now, open the /etc/exports file and add a new line for the backup directory as follows:<br>
<img src = "./Picture1.jpg">
