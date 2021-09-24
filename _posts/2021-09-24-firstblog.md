---
layout: post
title:  "Blog 1 - Slow server troubleshooting. Part 1"
date:   2021-09-24 13:55:28 -0700
categories: ubuntu blog
---
When it comes down to server performance, CPU health is one of the top things tokeep an eye on. When CPU is overloaded with tasks, its performance goes down. Therefore, your server becomes slow.<br>
Thankfully, there is a very useful command, that I just love to use, which is called `top`. Just go ahead and run `top` in your terminal, and it will give you real time information about the processes running on your server.<br> Top is extremely useful when you want to see what processes are taking up the most CPU  resources. Look out for runaway processes! `Top` command is going to show you how many processes are running, how much CPU each process is taking up, `load average`, and a lot of other inforamtion, that is outside of the  scope of this article. 
It is important to explain what `load average` means though.<br> 
Load average numbers represent the average CPU load in 1, 5, and 15 minute intervals. The CPU load is the <b>average number of processes that are waiting to be executed by the CPU</b>. Think about a single-core CPU as a single lane in traffic. When the lane is really busy, traffic is going to be at 100%. In CPU terms, it is going to be a load of 1.<br> What if there are twice the amount of cars on the road? In that case, we can say that our road is 200% occupied. In order to fit twice as many cars, we need one more lane, right? In CPU terms, it means one more core.<br> Now, at 200% occupancy our CPU load average is going to be 2. However, even if we have a two-core CPU, that doesn't mean that it  has to be 200% occupied at all times. Your load average may be 0.5, which means just 25% of your 2-core CPU is affected. <br>
Lastly, if you see a process that is taking more resources than it should, you can go ahead and kill it with `kill -9 PID`. You can find `PID` number of the process in `PID` column after you run the `top` command.
To be continued ...

