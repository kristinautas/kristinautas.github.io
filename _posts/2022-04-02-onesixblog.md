---
layout: post
title: "Blog 1.6  - Elastic Load Balancing "
date: 2022-04-02 14:21:28 -0700
categories: AWS blog
---

`Elastic Load Balancing` is an AWS service that distributes incoming <br>
application or network traffic across multiple targets (EC2 instances, <br>
 containers, IP addresses, and Lambda functions). `Elastic Load
 Balancing` <br>
 scales your load balancer as traffic to your application <br>
 changes over time. <br> <br>
There are 3 types of Elastic Load Balancing: <br><br>
•`An Application Load Balancer` operates at the application level. <br>
 It routes traffic to targets based on the content of the request. It is <br>
 ideal for advanced load balancing of HTTP and HTTPS traffic. An <br>
 `Application Load Balancer` provides advanced request routing that <br>
 is targeted at delivery of modern application architectures, including <br>
 microservices and container - based applications. An Application Load <br>
 Balancer simplifies and improves the security of your application by <br>
 ensuring that the latest `SSL/TLS` ciphers and protocols are always used. <br><br>
 
•A `Network Load Balancer` operates at the network transport level, <br>
 routing connections to targets (EC2 instances, microservices, and <br>
containers) based on IP protocol data. It works well for load balancing <br>
 both TCP and UDP traffic. A `Network Load Balancer` is optimized <br>
 to handle sudden and volatile network traffic patterns.  <br> <br>
•A `Classic Load Balancer` provides basic load balancing across <br>
 multiple EC2 instances, and it operates at both the application level <br>
 and network transport level. A `Classic Load Balancer` supports the <br>
 load balancing of applications that use HTTP, HTTPS, TCP, and SSL. <br>
 The `Classic Load Balancer` is an older implementation and not <br>
 recommended. <br> <br>
A `load balancer` accepts incoming traffic and routes requests to its <br>
targets. You configure your `load balancer` to accept incoming traffic <br>
 by specifying `listeners`. A `listener` is a process that checks for <br>
 connection requests. It is configured with a protocol and port number <br>
 for connections to the load balancer. Similarly, it is configured with a <br>
 protocol and port number for connections from the load balancer to the <br>
 targets. <br> <br>
You can also configure your `load balancer` to perform health checks, <br>
 which are used to monitor the health of the targets. When the load <br>
 balancer detects an unhealthy target, it stops routing traffic to that target <br>
 until it is healthy again. <br>
There is a key difference in how the `load balancer` types are configured. <br>
 With `Application Load Balancers` and `Network Load Balancers`, you <br>
 register targets in target groups, and route traffic to the target groups. <br>
With `Classic Load Balancers`, you register instances with the `load balancer`. 



<br><br>
References: <br>
AWS Academy Cloud Foundations <br>
Module 10: Auto Scaling and Monitoring <br>

