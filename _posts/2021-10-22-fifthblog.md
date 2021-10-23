---
layout: post
title: "Blog 4 - Processes in Linux. Part 1"
date: 2021-10-15 14:21:28 -0700
categories: ubuntu blog
---
Like promised, today I'm going to explain some dark Linux terms. So, sometimes,<br> 
a parent process dies before a child processes. In that case, what happens to <br> the child process? Well, kernel knows that it is not going to get a wait call<br>
from the parent because the parent is dead. Kernel needs to get that wait call though. <br>
So, what it does is it finds that child a new parent, which is `Init`. `Init` adopts the `orphan` and makes a wait call when that `orphan dies`. <br>
Besides `orphan` processes, I also promised to explain `zombie` processes. <br>
A process becomes a `zombie` when it dies, but its parent hasn't made a wait <br>call to the kernel yet. The future of this `zombie` process is either to wait <br>until the parent makes a wait call to the kernel and disappear or to be adopted <br>by the `Init` process and expect it to fulfill its parent's duties of<br> making a wait call to the kernel. <br>
Too many `zombie` processes can be a bad thing. It can prevent other processes from running by taking up space in the process table.<br>
Let's say, we want to force a process to finish. We can do that via commandline <br>
by running `kill` + `PID`. By default, it sends `TERM` signal to the process.<br>
You can also send `SIGKILL` signal to the process by using `-9` option with the `kill` command. These two signals are very similar, but they do have their differences. `SIGTERM` means  to kill the process, but allow it to do some cleanup first. `SIGKILL` means to kill the process, kill it with fire, no  cleanup.
~

Some of the other common signals are `SIGINT`, `SIGHUP` and `SIGSTOP`. `SIGHUP` is  sent to a process when the controlling terminal is closed. If you closed<br> a terminal window that had a process running in it, you would get a SIGHUP signal. <br>
`SIGINT` is an interrupt signal, so you can use Ctrl-C and the system will<br> try to gracefully kill the process<br>
`SIGSTOP` simply means stop/suspend a process.
