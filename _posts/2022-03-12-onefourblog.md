---
layout: post
title: "Blog 1.4  - AWS Identity and Access Management (IAM) "
date: 2022-03-12 14:21:28 -0700
categories: AWS blog
---
`AWS Identity and Access Management (IAM) ` allows to control access to compute, <br>
storage, database, and application services in the cloud. `IAM` handles <br>
`authentication` and `authorization.` `IAM` is a tool that centrally manages access to <br>
launching, configuring, managing, and terminating resources in your account. Every <br>
call to an AWS service is an API call. With `IAM,` you can manage which resources <br>
can be accessed by who, and how these resources can be accessed. You can grant <br>
different permissions to different people for different resources. For example, you can <br>
allow some users `full access` to Amazon EC2, Amazon S3, etc., while for other users, <br>
you can allow `read-only` access to the same resources. `IAM` is a feature of `AWS account, `  <br> and it is offered at no additional charge. It is important to understand the role and function <br> of each of the four `IAM components.` An `IAM user` is a person or application that is <br> defined in an `AWS account, ` and that must make API calls to AWS products. Each `user` <br> must have a unique name within the AWS account, and a set of security credentials. 
Each `user` is defined in one and only one AWS account. An `IAM group` is a collection of IAM <br> users. You can use `IAM groups` to simplify specifying and managing permissions for <br> multiple users. An `IAM policy` is a document that defines permissions to determine what users <br> can do in the AWS account. A policy grants access to specific resources and specifies <br> what the user can do with those resources. Policies can also explicitly deny access. An <br> `IAM role` is a tool for granting temporary access to specific AWS resources in an AWS <br> account.
<br> <br>

References:

<br>
AWS Academy Cloud Foundations Module 5: Networking and Content Delivery
