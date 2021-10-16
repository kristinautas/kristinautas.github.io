---
layout: post
title: "Blog 4 - Processes in Linux. Part 1"
date: 2021-10-15 14:21:28 -0700
categories: ubuntu blog
---
Simply put, a <b>program</b> is a <i>file</i> with a set of instructions. A<b> process</b> is an instance of a running program aka those instructions put in motion.<br>
The first process that is started on Linux OS when it boots up is <b>Init</b> process. <b>Init</> is the parent of all other processes, it doesn't have its own parent, and <br>
it always has process ID of 1 or PID 1. <br>
Ok, we know how the Init process starts, but how do all of the other processes start? Think of it as a family  tree, where every parent is single (sad, I know).<br>
Imagine, Init is the main parent at the top of this tree. Init has children (child processes), Init's children have children, children of Init's children have children etc. <br>You get the idea. Every time a child of some process gets its own child, it becomes a parent for that child, but keeps stayong a child to its own parent. <br>
Hopefully, you remember the process ID of Init. That's right, it is 1. So, what would be Init's child's PID? Process IDs are allocated on a sequential basis, so, let's say it's 2. In that case, we can say, that Parent Process ID (PPID) of Process ID (PID) 2 is 1. <br>
<br>
What happens when a process needs to terminate? Let's say, our PID 2 want to call it quits. In that case, it will make a system call to the kernel to let it know its <br>
termination status. However, that's not enough to complete the  termination process. Every parent would want to know why its child died, right? So it would make its own system call to the kernel to find out what the termination status of its child is. After a parent acknowledges the termination status, its child is officially dead.<br><br>
In the second part of our discussion about processes, Linix will get  even darker.. we are going to talk about zombies, orphans and adoption (: Stay tuned.
