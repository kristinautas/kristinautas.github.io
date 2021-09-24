---
layout: post
title:  "Blog 1 - Slow server troubleshooting. Part 1"
date:   2021-09-24 13:55:28 -0700
categories: ubuntu blog
---
When it comes down to server performance, CPU health is one of the top things tokeep an eye on. When CPU is overloaded with tasks, its performance goes down. Therefore, your server becomes slow. 
Thankfully, there is a very useful command, that I just love to use, which is called `top`. Just go ahead and run `top` in your terminal, and it will give you real time information about the processes running on your server. Top is extremely useful when you want to see waht processes are taking up the most CPU  resources. Look out for runaway processes! `Top` command is going to show you how many processes are running, how much CPU each process is taking up, `load average`, and a lot of other inforamtion, that is outside of scope of this article. 
However, it is important to explain here what `load average` means. 
Load average numbers represent the average COU load in 1, 5, and 15 minute intervals. The CPU load is the <b>average number of processes that are waiting to be executed by the CPU</b>If you see a process that is taking more resources than it should, you can go ahead and kill it with `kill -9 PID`. You can find `PID` number of the process in `PID` column after you run the `top` command.

