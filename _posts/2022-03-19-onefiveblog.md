---
layout: post
title: "Blog 1.5  - AWS Identity and Access Management (IAM). Continued "
date: 2022-03-19 14:21:28 -0700
categories: AWS blog
---
`Authentication` means proving one’s identity. When you want to get through <br>
airport security, you must present identification to prove who you are before you <br>
can enter a restricted area. Same concept applies for gaining access to AWS <br>
resources. When you define an `IAM user`, you select what type of access the user <br>
 is permitted. There’re two types of access to users: `programmatic access` and `AWS <br>
Management Console` access. You can assign `programmatic access only`, `console <br> access only`, or you can assign both types of access. If you grant `programmatic access`,<br> the IAM user will be required to present an `access key ID` and a `secret access key` <br> when they make an AWS API call by using the AWS CLI, the AWS SDK, or some other <br> development tool. If you grant `AWS Management Console access`, the `IAM user` will be <br>
required to fill in `login credential`s in the browser window. `If multi-factor authentication <br> 
(MFA) ` is enabled for the user, they will also be prompted for an `authentication code`. AWS <br> services and resources can be accessed by using the `AWS Management Console`, the <br> AWS CLI, or through `SDKs` and `APIs`. For increased security, `MFA` is recommended. <br> With `MFA`, users and systems must provide an `MFA token` before they can access AWS services and resources. <br><br>
`Authorization` is the process of determining what permissions a user, service or application <br> should be granted. After a user has been `authenticated` , they must be `authorized` to <br> access AWS services. By default, `IAM users` do not have permissions to access any <br> resources or data in an AWS account. Instead, you must explicitly grant permissions to a <br> user, group, or role by creating a `policy`. A `policy` lists permissions that allow or deny <br> access to resources in the AWS account. To assign permission to a `user, group or role`, <br> you must create or use an existing `IAM policy`. There are no default permissions. All actions <br> in the account are denied to the user by default. Any actions that you do not explicitly allow <br> are denied. Any actions that you explicitly deny are always denied. <br><br>
The `principle of least privilege` means that you grant only the minimal user privileges to the <br> user, based on the needs of your users. When you create `IAM policies`, it is a `best <br>practice` to grant `least privilege`. Determine what users need to be able to do and then <br> create policies for them that let the users perform only those tasks. Start with a minimum <br> set of permissions and grant additional permissions as necessary. IAM settings apply <br> across all AWS Regions.


<br><br>
References: <br>
AWS Academy Cloud Foundations <br>
Module 4: AWS Cloud Security <br>

