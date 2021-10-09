---
layout: post
title:  "What is a deadlock in Linux?"
date:   2021-10-08 14:21:28 -0700
categories: ubuntu blog
---
Let's talk about deadlock. If you want to become a linux administrator or just use linux-based environment at work, deadlock is something you should be aware of. <br>
Normally, resources are being used by processes in the followig manner: <br>
<b>1. Resource requested</b><br>
<b>2. Resource used</b><br>
<b>3. Resource released </b><br>
Deadlock is a special situation where certain processes can't finish executing because they are waiting for each other to give up resources that they both need in order to finish and none of them are giving them up.<br>
Imagine there are two people that want to eat their lunch, but there's only one set of utensils. One person is holding on to a knife, and another one is holding on to a fork.<br> None of them can start eating because they don't have a full set, and both of them can't give up their utensil before they finish eating.<br> Get the idea?<br>
There are four conditions that have to take place simultaniously for deadlock to arise:<br>
<b>1.Mutual Exclusion:</b> resources in question can't be shared (for example, printer)<br>
<b>2.Hold and Wait:</b> a process is holding on to at least one resource and waiting for at least one more to finish executing<br>
<b>3.No Preemption:</b>a resource can't be taken away from the process unless the process releases it<br>
<b>4.Circular Wait:</b>processes involved are waiting for each other in a circular manner<br>
<br>
In order to prevent deadlock, we need to eliminate any of the above conditions. Going over prevention of deadlock is outside of the scope of this article, however, it is worth mentioning <br>that mutual exclusion, for example, can't be eliminated because some resources, such as printer are non-shareable. <br> Prevention is better that cure anyway, right? Deadlock can be completely avoided by using resource allocation and deadlock avoidance algorithm called Banker's Algorithm. BA checks if it is safe to allow the request made by the process, and if it's not, it doesn't allow it.
