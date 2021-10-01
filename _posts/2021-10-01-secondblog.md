---
layout: post
title:  "Blog 2 - Slow server troubleshooting. Part 2"
date:   2021-10-01 14:21:28 -0700
categories: ubuntu blog
---
In the Part 1 we talked about CPU health monitoring. There are two more very important factors that can affect server speed.<br> 
One of them is input/output parameters. There's a handy tool for checking them  called `iostat`. <br>`iostat` will show us some of the CPU parameters as well, however, today we are going to focus on disk utilization. The second part of the `iostat` command output is going to show us the following parameters:<br>
<b>tps</b> - Indicate the number of transfers per second that were issued to the device. A transfer is an I/O request to the device. <br>
<b>kB_read/s</b> - Indicate the amount of data read from the device expressed in kilobytes per second. <br>
<b>kB_wrtn/s</b> - Indicate the amount of data written to the device expressed in kilobytes per second. <br>
<b>kB_read</b> - The total number of kilobytes read.<br>
<b>kB_wrtn</b> - The total number of kilobytes written.<br>
Storage input and output statistics are very important in identifying performance issues with storage devices.<br><br>

