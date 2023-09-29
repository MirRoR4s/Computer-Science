# Linux Services

在本课程的第二个模块中，我们将讨论Linux操作系统中可用的服务。 

In the second module of this course, we will discuss the services available in the Linux operating system. 

我们将探索许多服务，包括web服务器和数据库服务器等等。  

We will explore many services including web servers and database servers, among others. 

我们将介绍如何在Linux操作系统中启动和停止服务。  

We will look at how you start and stop services from running in the Linux operating systems.

**学习目标**Learning Objectives 

- 请列出Linux操作系统提供的几种服务 List the several services provided by the Linux operating system
- 描述几个在 Linux 中可用的Web服务器 Describe several Web Servers available in Linux
- 描述几个在 Linux 中可用的数据库服务器 Describe several Database Servers available in Linux
- 启动和停止服务 Start and Stop services

## [Servers vs Desktops](https://www.coursera.org/learn/linux-fundamentals/lecture/aDeRH/servers-vs-desktops)

### Video: Servers vs Desktops

欢迎回到Linux基础。 

Welcome back to Linux Fundamentals. 

这是Linux基础专门化的第一门课程。  

This is the first course in the Linux Foundation Specialization. 

在这个模块中，我们要考虑Linux服务。  

In this module, we want to think about Linux services. 

---

学习完这个模块后，进行测验时，你应该能够做以下事情:你应该能够列出 Linux 操作系统提供的几个服务; 

By the time you're done with this module, when you take the quiz, you should be able to do these things: you should be able to list several services provided by the Linux operating system. 

您应该能够描述在Linux中可用的几个web服务器。  

You should be able to describe several web servers available in Linux. 

您应该能够描述Linux中可用的几个数据库服务器，最后，您应该能够启动和停止服务。  

You should be able to describe several database servers available in Linux, and lastly, you should be able to start and stop services. 

在第1课中，我们要区分服务器和台式机。  

In lesson 1, we want to distinguish between server and desktop. 

服务器专注于提供共享资源的程序，我们称之为服务。  

Servers focus on programs that provide shared resources, we call those services. 

台式机专注于运行在图形用户界面中的程序。  

Desktops focus on programs that run in a graphical user interface. 

我们称之为GUI。  

We call that a GUI. 

想想 macOS 和 Windows ，它们是典型的桌面操作系统。  

Think about macOS and Windows, these are typical desktop operating systems. 

这是真的，你可能会说 Windows 有服务器操作系统，这是真的，但 GUI 实际上是用于台式机的。 

Now it's true, you might say Windows has server operating systems, it's true, but the GUI is really for the desktops. 

在本课程中，我们将主要考虑使用Linux作为服务器。  

In this course, we're going to think about primarily the use of Linux as a server. 

我们将考虑这些共享资源和服务。  

We're going to think about these shared resources and services. 

服务器运行服务程序有两种主要方式。  

There are two primary ways servers run service programs. 

第一个是始终运行监听请求的后台进程。  

The first is a background process that's always running listening for request. 

另一种是由监听请求的父程序派生的进程。  

The other is as a process spawned by a parent program that listens for request. 

父进程在监听，一个请求进来，它启动一个新的子进程来处理这个请求，这样它就可以继续监听来自其他客户端的新请求。  

The parent is listening, a request comes in, it spins up a new child to service that request so that it can continue listening for new requests coming in from other clients. 

您将在《Linux中的服务》中听到“守护进程”这个术语。  

You're going to hear this term **deamon** referred to in services in Linux. 

什么是守护进程?  

What is a deamon? 

当一个 Linux 服务作为后台进程持续运行时，它被称为守护进程。  

When a Linux service runs continually as a background process, it is called a deamon. 

Linux 的守护进程通常以字母d结尾。例如，mysqld是一个守护mysqld数据库的程序。  

Linux deamons often end with the letter d. For example, mysqld is the program that's a demon for the mysqld database.

---

有几种主要的服务类型。 

There are several major service types available. 

我们有文件服务器，打印服务器，网络服务器，数据库服务器，邮件服务器。  We have file servers, print servers, web servers, database servers, mail servers. 

现在，你们都可以认为网络上主机的默认名称是www，代表web服务器。  Now, you all can think about the default name of a host on the web is www, that stands for web server. 

那时候办公室里有一个文件服务器，通常叫file，还有一个打印服务器，叫print然后web就出现了，万维网，也就是web服务器。  This comes from the days where in the office you would have a file server, often called file and a print server called print and web came along, which was World Wide Web, that was web server. 

我们有各种各样的服务器，可能是一台机器，也可能有单独的机器，也可能有多台机器来处理负载。  

We have all different kinds of servers, maybe a one machine, they may have separate machine, may have multiple machines to service the load. 

但我们有这些不同的主要服务类型。  

But we have these different major service types. 

我们也有网络资源服务器。  

We also have network resource servers. 

这些是补充服务，帮助支持诸如分配地址，日志记录之类的事情。  

These are supplemental services that help support things like assigning addresses, logging, those sorts of things. 

这里回顾一下。  A little review here. 

Linux桌面有围绕GUI交互应用程序设计的程序，图形用户界面。  

Linux desktop has programs designed around GUI interactive applications, graphical user interface. 

Linux服务器有围绕共享资源的后台服务设计的程序，而守护进程的名字通常以字母d结尾，以帮助我们看到它何时运行，它是一个守护进程还是一个交互式程序。  

A Linux server has programs designed around background services that share resources, and deamons often end with the letter d in their name to help us see when it's running, that it's a deamon versus an interactive program. 

下节课见。  

See you in the next lesson.

## Web Servers

### Video: Web Servers

欢迎回到Linux服务。 

Welcome back to Linux services. 

这一课，我们将深入研究运行Linux服务器的一个非常具体和常见的服务Web服务器。  

In this lesson, we're going to drill into a very specific and common service that's running Linux Servers Web Servers. 

我在前面的模块中说过，90%的云运行在Linux服务器上。  

I said earlier in a previous module that 90% of the cloud runs on Linux Servers. 

很多web服务器，web服务器可以监听80或443端口，它们可以监听任何端口。  

And so a lot of those our web servers, So web servers sit and listen on either port 80 or 443, they can actually listen to any port. 

但这是两个常见的值，80 表示未加密，443 表示SSL或HTTPS连接。  

But these are the two common ones 80 is for non encrypted, 443 is for SSL or HTTPS connections. 

当一个传入的请求进来时，它们将请求分配给一个进程并返回响应?  

And when an incoming request comes in, they assign the request to a process and return the response, okay? 

在Lenox上有三个主要的web服务器，Apache, nginX和Lighttpd。  

There are three major web servers available on Lenox, Apache, nginX and Lighttpd.