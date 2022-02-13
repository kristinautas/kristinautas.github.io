---
layout: post
title: "Blog 1.0  - "Amazon Virtual Private Cloud (VPC) Overview"
date: 2022-12-19 14:21:28 -0700
categories: AWS blog
---
There’s no doubt in the fact that more and more companies are moving their resources to the cloud. It’s <br>important for a future IT professional to be familiar with cloud concepts, and that’s exactly what the <br>next few blog posts are going to help you with. <br><br>Today, we will learn about `VPC` and <br>some of its fundamental components. Many of the concepts of a physical network apply to a cloud-<br>based network. For instance, `Amazon Virtual Private Cloud (Amazon VPC) ` is a service that lets <br>you create a logically isolated section of the AWS Cloud that is similar to your physical database. <br>After you create a VPC, you can divide it into subnets. <br><br>
Subnets may be private or public. `Public subnets` have direct access to the internet, `private subnets` do <br>not. Network traffic from your subnet is directed by a set of rules (routes) in a `route table`. Each <br>route specifies a `destination` and a `target`. The destination is the CIDR block where you want <br>traffic from your subnet to go. The target is the target that the destination traffic is sent through (for <br>example, an `internet gateway`). By default, every `route table` that you create contains a `local <br>route`. You can add `routes` to your `route tables`. You cannot delete the local route entry that is <br>used for internal communications. Each subnet in your VPC must be associated with a `route table`. <br>The `main route table` is the `route table` is automatically assigned to your `VPC`. It controls the <br>`routing` for all subnets that are not explicitly associated with any other `route table`. A `subnet` can <br>be associated with only one `route table` at a time, but you can associate multiple `subnets` with the <br>same `route table`. <br><br>An `internet gateway` is a `VPC` component that allows <br>communication between instances in your `VPC` and the internet. An `internet gateway` provides a <br>`target` in your `VPC route tables` for internet-routable traffic and performs `network address <br>translation` for instances that were assigned public IPv4 addresses. To make a subnet public you attach an `internet gateway` to your `VPC` and add a `route` to the `route table` to send non-local traffic <br>through the `internet gateway` to the internet (0.0.0.0/0). <br><br>
A `network address translation (NAT) gateway` enables instances in a `private subnet` to connect to the <br>internet or other AWS services but prevents the internet from initiating a connection with those <br>instances. To create a `NAT gateway`, you must specify the `public subnet` in which the NAT <br>gateway should reside. You must also specify an `Elastic IP address` to associate with the `NAT <br>gateway` when you create it. After you create a `NAT gateway`, you must update the `route table` <br>that is associated with one or more of your `private subnets` to point internet-bound traffic to the `NAT gateway`. This way, instances in your `private subnets` can communicate with the internet. <br>

