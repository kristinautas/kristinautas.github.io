---
layout: post
title: "Blog 1.2  Amazon Route 53"
date: 2022-02-26 14:21:28 -0700
categories: AWS blog
---
`Amazon Route 53` is a cloud `Domain Name System`  <br>
 web service. Just like any `DNS`  it `Route 53` provides <br>
 a way to route users to internet applications by translating <br>
 names into the IP addresses. `Amazon Route 53` <br>
 connects user requests to `EC2 instances`, load <br>
 balancers, or `S3 buckets`. It can also route users to <br>
 infrastructure that is outside of AWS. You can use <br>
 `Amazon Route 53` to configure health checks of your <br>
 endpoints, or you can use other services for that same <br>
 thing. `Amazon Route 53` helps to manage traffic globally <br>
 and offers options for low-latency and fault-tolerant <br>
architectures. The following are the types of routing policies <br>
 that define how `Amazon Route 53` responds to queries: <br>
`• Simple routing (round robin)` – Use for a single resource <br> <br>
 that performs a given function for your domain <br>
`• Weighted round robin routing` – Use to route traffic to <br> <br>
 multiple resources in proportions that you specify. Enables <br>
 you to assign weights to resource record sets to specify <br>
 the frequency with which different responses are served. <br>
 You might want to use this capability to do testing.  <br>
`• Latency routing (LBR)` – Use when you have resources <br> <br>
 in multiple AWS Regions and you want to route traffic to <br>
 the Region that provides the best latency.  <br> <br>
`• Geolocation routing` – Use when you want to route traffic <br>
 based on the location of your users. When you use <br>
 geolocation routing, you can localize your content and <br>
 present some or all your website in the language of your users. <br>
You can also use geolocation routing to restrict the <br>
 distribution of content to only the locations where <br>
you have distribution rights. Another possible use is for <br>
 balancing the load across endpoints in a predictable,  <br>
easy-to-manage way, so that each user location is consistently <br>
 routed to the same endpoint.  <br> <br>
`• Geoproximity routing` – Use when you want to route traffic <br>
 based on the location of your resources and shift traffic from <br>
resources in one location to resources in another.  <br> <br>
`• Failover routing (DNS failover)` – Use when you want <br>
to configure failover. `Amazon Route 53` can help detect an <br>
 outage of your website and redirect your users to alternate <br>
 locations where your application is operating properly. <br> <br>
`• Multivalue answer routing` – Use when you want `Route 53` <br>
 to respond to DNS queries with up to eight healthy records <br>
 that are selected at random. You can configure `Amazon` <br>
`Route 53` to return multiple values, such as IP addresses <br>
 for your web servers in response to `DNS queries`. <br>
You can specify multiple values for almost any record. <br>

<H14> References: </H14> <br>
<H14> AWS Academy Cloud Foundations 
Module 5: Networking and Content Delivery </H14>

