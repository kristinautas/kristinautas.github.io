---
layout: post
title: "Blog 1.1  - "Security Groups and Acess Control Lists in AWS"
date: 2022-02-19 14:21:28 -0700
categories: AWS blog
---
As you may already know, security comes in layers. That is to ensure that <br>
 each individual component of your security plan has a backup in case the <br>
 other ones fail. Also, it creates more obstacles that one must overcome <br>
 to get to your resources. <br> <br>
So, there is usually more than just one `firewall` that controls the traffic going <br>
 in and out of your network. In AWS, there’re two `firewall` options that can <br>
 be used for a VPC security: `security groups` and `Access Control Lists (ACL) ` . <br>
 `Security group` is a virtual `firewall` that controls the traffic flow at an instance <br>
 level.  `Security groups` have rules that provide control of both `incoming` and <br>
 `outgoing traffic` .  By default, `security groups`  `allow` all `outbound traffic` and <br>
 `deny` all `inbound traffic` , but you can change that but changing `rules` . You can <br>
 set `allow rules` but not `deny rules` for your `security groups` . <br> <br>
`Security groups` are `stateful` . There’s usually a lot of confusion when it comes <br>
 down to `stateful` vs `stateless firewalls` , so let me clear that up for you. Simply <br>
 put, `stateful firewalls` keep information about the `requests` even after they <br>
 have already been processed. For example, we know that all `inbound traffic` <br>
 is `not allowed` by default. However, if your instance initiates the `request` , the <br>
`response traffic` for that `request` will be `allowed` regardless of the `inbound` <br>
 `traffic rules` . Similarly, `responses` to `allowed inbound traffic` are `allowed` to go <br>
 out, regardless of `outbound rules` . This ability to keep track of the information <br>
 about `requests` makes a `firewall stateful` . <br> <br>

`A network access control list (network ACL) ` is another layer of security for  <br>
your VPC. It acts as a `firewall` for controlling `traffic ` at subnet level. <br>
You can set up network `ACLs` with `rules` that are the same as your `security` <br>
 `groups` or different. By default, it `allows` all `inbound` and `outbound traffic` . <br>
In a network `ACL` each `rule` can either `allow` or `deny traffic` . <br>
Unlike `security groups` , Network ACLs don’t keep any information about a  <br>
`request` after a it is processed, which makes it `stateless` . <br> <br>
There’re a few key points that you need to take away from this article: 1. Level
 at which each security layer operates. 2. Difference between `stateful` and
 `stateless firewalls` . 3. What type of `rules` each `firewall` supports (`allow` and `deny
rules`). 

