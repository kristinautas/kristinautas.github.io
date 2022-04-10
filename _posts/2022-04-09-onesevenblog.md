---
layout: post
title: "Blog 1.7  - Amazon EC2 Autoscaling "
date: 2022-04-09 14:21:28 -0700
categories: AWS blog
---
`Scaling` is the ability to increase or decrease the compute capacity <br>
 of your application. In the cloud, because computing power is a <br>
 programmatic resource, you can take a flexible approach to scaling. <br>
`Amazon EC2 Auto Scaling ` is an AWS service that helps you maintain <br>
 application availability and enables you to automatically add or remove <br>
 `EC2 instances ` based on your needs. `Amazon EC2 Auto Scaling `  <br>
provides several ways to adjust scaling to best meet the needs of your <br> 
applications. You can add or remove `EC2 instances ` manually, on a <br>
schedule, in response to changing demand, or in combination with `AWS` <br>
`Auto Scaling` for predictive scaling. Capacity scaling is necessary to <br>
support the fluctuating demands for service. Without scaling, the servers <br>
could crash due to saturation, which is never good. <br><br>

An `Auto Scaling group ` is a collection of `Amazon EC2 instances` that <br>
are treated as a logical grouping for the purposes of automatic scaling <br>
and management. The size of an `Auto Scaling group ` depends on the <br>
number of instances you set as the desired capacity. You can adjust its <br>
size to meet demand, either manually or by using `automatic scaling `. <br>
You can specify the minimum number of instances in each `Auto Scaling` <br>
`group`, and `Amazon EC2 Auto Scaling ` is designed to prevent your <br>
group from going below this size. You can specify the maximum number of <br>
 instances in each `Auto Scaling group `, and `Amazon EC2 Auto Scaling ` <br>
is designed to prevent your group from going above this size. If you specify <br>
the desired capacity, either when you create the group or at any time <br>
afterwards, Amazon `EC2 Auto Scaling ` is designed to adjust the size of <br>
your group so it has the specified number of instances. If you specify <br>
scaling policies, then `Amazon EC2 Auto Scaling ` can launch or terminate <br>
 instances as demand on your application increases or decreases. <br> <br>
To launch `EC2 instances `, an `Auto Scaling group ` uses a `launch` <br>
`configuration`, which is an instance configuration template. When you <br>
create a `launch configuration `, you specify information for the instances <br>
such as the ID of the `Amazon Machine Image `, the `instance type `, `AWS <br>
Identity and Access Management role `, `additional storage `, one or more <br>
 `security groups `, and any `Amazon Elastic Block Store volumes `. You <br>
define the minimum and maximum number of instances and desired <br>
capacity of your Auto Scaling group. Then, you launch it into a subnet <br>
within a VPC. Amazon EC2 Auto Scaling integrates with Elastic Load <br>
Balancing to enable you to attach one or more load balancers to an existing <br>
Auto Scaling group. After you attach the load balancer, it automatically <br>
registers the instances in the group and distributes incoming traffic across <br>
the instances. 

<br><br>
References: <br>
AWS Academy Cloud Foundations <br>
Module 10: Auto Scaling and Monitoring <br>

