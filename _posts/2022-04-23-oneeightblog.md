---
layout: post
title: "Blog 1.9  - Containers (Docker) "
date: 2022-04-23 14:21:28 -0700
categories: AWS blog
---
`Containers` are a method of operating system `virtualization` <br>
that enables you to run an application and its dependencies <br>
in resource - isolated processes. `Containers` are smaller than <br>
 virtual machines, and do not contain an entire operating system. <br>
They have everything that the software needs to run, such <br>
as libraries, system tools and code. `Containers` deliver <br>
environmental consistency because the application’s code, <br> configurations, and dependencies are packaged into a single <br>
object. `Container images` are smaller than `virtual machines` . <br>
Spinning up a `container` takes less than a second. They are fast and <br> portable. `Containers` can help ensure that applications deploy <br> quickly, reliably, and consistently, regardless of the environment. <br> `Containers` also give you more granular control over resources. <br>They are a little bit different than `virtual machines` . <br>
Typically, in a `VM-based deployment` , multiple EC2 instances run <br>
directly on the `hypervisor` and each of them runs a virtual machine. <br>In a `VM-based deployment`, each app would run on its own `VM` to <br> provide process isolation. In a `container-based deployment`, there <br>would only be one EC2 instance. The `Docker engine` is installed on <br> the Linux guest OS of the EC2 instance, and there are multiple <br> `containers`. In the container-based deployment, each app runs in <br> its own `container` , which provides process isolation, but all the <br> `containers` run on a single EC2 instance. The processes that run <br> in the containers communicate directly to the kernel in the Linux <br> guest OS and are largely unaware of other containers. The `Docker <br> engine` makes it easier to manage how the containers run on the <br> Linux <br> guest OS, they are also more disposable. <br>
<br> In an actual container-based deployment, a large EC2 instance <br> could run hundreds of containers.

<br><br><br><br>
AWS Academy Cloud Foundations
Module 6: Compute


