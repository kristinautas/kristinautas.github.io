---
layout: post
title: "Introduction to Linux Security"
date: 2021-11-12 14:21:28 -0700
categories: ubuntu blog
---

In short, securing a host or network means applying controls to users’ and processes’ <br>ability to gain access to computer resources, such as files, devices, and interfaces. <br>In Linux there is a good number of <b>Access Control Mechanisms (ACMs)</b>. <br>. Let’s take a look at them. <br>
<b>Discretionary Access Control (DAC) </b> deals with access to filesystem objects (files, <br> directories, devices). It provides the ability to grant access at owner’s <br>discretion. This means that when a user creates an object, they can grant access <br>to it as they choose based on the identity of users and groups.<br>
<b>Access Control Lists (ACLs)</b> control which users and groups have <br>access to specific files and directories.<br>
<b>Mandatory Access Control (MAC)</b> provides different levels of access control. <br> MAC adds additional categories to all filesystem objects. This way, subjects must <br>have access to these categories to interact with the objects that belong to those <br>categories. MAC is enforced by <b>SELinux</b> which we will talk about in later blog posts.<br>
<b>Role-Based Access Control (RBAC)</b> means that instead of permissions, access <br>to filesystem objects is based on roles. Roles could be based on some business or <br>functional purpose. RBAC gives access based on logic, much like group policies in Windows. <br> Subjects must be members of a specific group before they can interact with certain objects.<br>
<b>Multi-Level Security (MLS)</b> is a type of MAC where the subjects are<br> processes and the objects are files, sockets, and other system resources.<br>
<b>Multi-Category Security (MCS)</b> is an enhanced version of SELinux that allows users to label files with categories. MCS reuses much of the MLS framework in SELinux. <br>
Today, we covered some mechanisms that Linux uses to control access to its <br>resources. In the next blog, we’ll discuss SELinux – security framework in the Linux <br>kernel that is used for managing the access control policies of resources. 
.


