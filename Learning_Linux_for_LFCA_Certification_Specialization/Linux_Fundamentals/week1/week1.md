# Linux Operating System

- 地址：https://www.coursera.org/learn/linux-fundamentals/home/week/1

欢迎来到 Linux 操作系统，这是 Linux 基础专业的第一门课程。 Welcome to Linux Operating System, the first course of the Linux Fundamentals specialization. 

通过报名参加这门课程，你将踏出你信息技术事业的第一步。  By enrolling in this course, you are taking the first step to kick start your career in information technology. 

在课程的第一周，我们将了解 Linux 操作系统的历史、其独特的许可模型和可使用的重大的发行版。  In the first week of the course, we will learn about the history of the Linux operating system, its unique licensing model and the major distributions that are available to use. 

在本模块结束时，您将了解如何选择一个发行版，安装它并登录到命令行。  By the end of this module, you will know how to choose a distribution, install it and login to the command line. 

那么，让我们开始吧!  So, let us get started!

**学习目标 Learning Objectives**

- 描述 Linux 操作系统的历史 Describe the history of the Linux Operating System
- 弄清楚 Linux 许可模式及其对 Linux 操作系统的成功产生的影响 Define the Linux licensing model and its effect on the success of the operating system
- 描述主要的Linux发行版 Describe Major Linux Distributions
- 登录Linux命令行 Login to a Linux Command Line

## Specialization Overview

### Specialization Overview-视频

欢迎来到Linux基础专业。 Welcome to the Linux Foundation Specialization. 

在这个专业中，有四门课程涵盖了Linux管理的基础。  

In this specialization are four courses that cover the foundations of Linux administration. 

在完成本专业后，我希望你能够做几件事。 

 Upon completion of this specialization, I want you to be able to do several things. 

您应该能够查看、创建、复制、移动和删除 Linux 系统中的文件，您应该能够搜索和分析Linux系统中的文本，您应该能够配置网络连接用户和组，您应该能够管理磁盘和软件包，您应该能够保护Linux系统。  

You should be able to view, create, copy, move, and remove files from your Linux system, you should be able to search and analyze text in Linux system, you should be able to configure network connections users and groups, you should be able to manage disks and software packages, you should be able to secure that Linux system. 

我们将讨论内部保护、权限、身份验证和授权，以及外围安全性，您应该能够比较和对比云计算模型、虚拟化和容器。  

We'll talk about both securing it internally, the permissions, authentication and authorization, but also perimeter security, and you should be able to compare and contrast cloud computing models, virtualization and containers. 

上述三个术语是我们今天在使用 Linux 时经常听到的流行语，我希望您能够真正理解它们，并思考哪个是您正试图解决的问题的正确解决方案。  These are buzzwords we hear a lot of today that use Linux, but I want you to really be able to understand them and think about which is the right solution for the problem you're trying to solve. 

在这个专业中，第一门课程是 Linux 基础，第二门课程是管理 Linux 系统，然后我们将探究如何保护 Linux系统，然后我们将在第四门课程中总结 Linux 云和 DevOps。  

In this specialization, the first course is Linux fundamentals, the second course is managing Linux systems, we'll then follow up with securing Linux systems, and then we'll conclude with Linux Cloud and DevOps in the fourth course. 

还有另外两门课程不是这个专业的一部分，但被捆绑在一起，我们称之为 LFCA 的专业证书，Linux基金会认证IT助理。  There are two other courses that are not part of this specialization but are bundled together in what we call the Professional Certificate for LFCA, Linux Foundation Certified IT Associate. 

这是一种专业认证，你可以参加考试，测试你对基本 IT 概念的知识，包括操作系统、软件应用程序安装管理、硬件安装、命令行和基本编程的使用、基本网络功能、安全最佳实践和其他相关主题，以验证你的能力，并为入门级 IT 职位做好准备。  That's a professional certification out there, and you can take an exam that will test your knowledge of fundamental IT concepts, including operating system, software application installation management, hardware installation, use of the command line and basic programming, basic networking functions, security best practices and other related topics to validate your capability and preparedness for an entry level IT position. 

我在这里有一个链接，所以你可以得到更多关于认证的信息。  I have a link here, so you can get to more information about certification. 

● htfps://training.linuxfoundation.org/certification/certified-it-associate/

但是有两门课程是与这个专业相结合的，一门是实践课程，我们会有更多的实验机会来实践你们应该知道的东西。  But there's two courses combined with this specialization, one is a practice where we'll have more lab opportunities to practice the things you should know for this certification. 

最后是考试准备，我们会有一些样题，我们会在课程中讨论考试。  Lastly is an exam prep, where we'll have some sample tests and we'll talk about the exam in that course. 

我希望你喜欢本专业，并学到很多东西。  I hope you enjoy specialization and learn a lot. 

课上见。  See you in the courses.

# History of Linux

欢迎来到Linux基础。 Welcome to Linux Fundamentals. 

Linux 基础是 Linux 基础专业的第一门课程。  Linux Fundamentals is the first course in the Linux Foundation Specialization. 

第一个模块我们将思考 Linux 操作系统。  The first module here we're going to think about the Linux operating system. 

当完成第一个模块时我希望你能做很多事情。  By the time we're done with this first module is many things I want you to be able to do. 

我的意思是，我希望你能够做到的事情，你应该能够做到，但你们也应该能够通过小测验和测试中的评估。  What I mean by things I want you to be able do, you should be able to do them, but you should also be able to be assessed on them in the quizzes and tests. 

您应该能够列出几个 Linux 发行版，应该能够描述 Linux 服务，应该能够查看、创建、复制、移动和删除 Linux 文件系统上的文件。  You should be able to list several Linux distributions, you should be able to describe Linux services, you should be able to view, create, copy, move, and remove files on the Linux file system. 

最后，您应该能够搜索和分析文本。  Lastly, you should be able to search and analyze text. 

在第一课中，我们将思考 Linux 的历史。  In this first lesson, we're going to think about the history of Linux. 

首先，什么是 Linux ?  

First off, what is Linux? 

当提到 Linux 时，指的是开源的类 unix 操作系统家族中许多特定发行版中的某一个。 

When we say Linux, we mean one of many specific distributions in a family of open source Unix-like operating systems. 

它们都基于 Linus Torvalds 开发的 Linux 内核。  

They're all based on the Linux kernel that was developed by Linus Torvalds. 

这些通常被捆绑在我们所谓的 Linux 发行版中。  

These are typically bundled in what we call Linux distribution. 

我们将在这个模块中讨论这些术语。  

We'll talk about all these terms through this module. 

不要对我刚才说的那些有意义的东西感到有压力，我们马上就会讲到。  

Don't stress a lot of what I just said that make sense, we're going to get there. 

Linux 最初是为个人计算机开发的，它是 X86 架构。  

Linux was originally developed for the personal computer, which is the X86 architecture. 

这和我们现在用于 Windows 电脑和 Macintosh 电脑的架构是一样的。  

That's the same architecture that we use for Windows machines, for Macintosh machines today. 

X86 是一种非常流行的用于家庭的架构。  

Very popular architecture used in home. 

然后它（Linux）被移植到许多其他平台。  

It was then ported to many other platforms. 

典型的例子有互联网上的服务器，以及现在非常成功的云。  

These are typically servers that are out in the Internet, in the Cloud today.  Very successful. 

Linux 也用在安卓系统中。  

It's also used in Android. 

安卓是谷歌的智能手机，它至少占据了一半的智能手机市场，使用的是 Linux 。  

Android, which is google smartphone, which has at least half of the smartphone market, uses Linux. 

chromebook，从谷歌那里再次流行起来。  

Chromebooks, which had become very popular again from Google. 

他们有一个使用 Linux 的 Chrome 操作系统。  They have a Chrome OS that uses Linux. 

许多嵌入式系统也运行在 Linux 之上。  

Many embedded systems also run Linux. 

大约 90% 的云基础设施是由 Linux 提供支持的。  

About 90 percent of all the Cloud Infrastructure is powered by Linux. 

Linux 就在那里，非常流行，对我们的社会非常重要。  

Linux is out there, very popular and very important to our society. 

让我们回过头来思考一下这些嵌入式系统。  Let's take a step back and think about those embedded systems. 

有许多不同的嵌入式系统。  There are many different embedded systems. 

不同的是通用系统就是我们所说的个人电脑。  The difference is a generic system is what we call personal computer. 

你可以用它做很多事情。  You can use it for many things. 

你可以用它来创作音乐，看视频，学习，做 Excel 和会计，诸如此类的事情，编程。  You can use it for creating music, for watching videos, for learning, for doing Excel and accounting, those sorts of things, for programming. 

这是通用的。  It's generic. 

嵌入式系统只有一个目的。  Embedded systems have one purpose. 

一些例子有家庭路由器或公司的路由器，它将在你的私有网络和公共网络之间路由流量。  Some examples are a home router or a router in your company, it's going to route traffic between your private network and your public network. 

工业自动化控制系统，智能家居技术，像我们今天的恒温器或洒水系统，我们所有的电视现在都有一个嵌入式系统，所以我们可以安装像 Peacock 或 Netflix 和亚马逊 Prime 这样的频道。  Automation control systems in industry, smart home technology, things like our thermostats today or sprinkler systems, all of our televisions now come with an embedded system so we can install channels like Peacock or Netflix and Amazon Prime. 

在我们的电视发布后，新频道会随之开发或更新。  New channels can come along that are developed or updated after our television has been released. 

我们的汽车有很多嵌入式系统，我们的数字录像机，我们的视频游戏机，我们的智能手表，现在无处不在，它将继续增长，其中很多都运行 Linux。  Our automobiles have many embedded systems, our digital video recorders, our video game console, our smartwatches right there, everywhere nowadays and it's going to keep growing and a lot of these run Linux. 

Linux 有何不同?  How is Linux different? 

与其他操作系统相比，Linux 有许多优点。  

Linux has many advantages over other operating systems. 

**这包括，它是开源的。**  

This includes, it's open-source. 

现在我们将深入研究开放源代码的含义。  

Now we're going to drill into what we mean by open source. 

通过一句话总结就是，您可以看到源代码，对源代码进行更改并与其他人共享。  

But the one-liner is, you're able to see the source code, make changes and share it with other people. 

其他操作系统则不是这样。  

That's not true of other operating systems. 

我们会回到这个问题。  

We'll come back to this. 

**它是由社区支持的。**  

It's community supported. 

因为它是开源的，很多人可以提供支持。  

Because it's open source lots of people can provide support. 

您不会被锁定在一个供应商的支持。 

 You're not locked into one vendor for support. 

**它支持较旧的硬件。**  

It supports older hardware. 

在另一个世界里，操作系统总是试图让你升级你的硬件。  

In the other world, the operating systems try to get you to upgrade your hardware all the time. 

这会变得很昂贵。  

That becomes expensive. 

Linux实际上可以在较旧的机器上运行。  

Linux will actually work on older machines. 

想想 Linux 的前身，Unix 是在 1969 年由贝尔实验室开发的。  

To think about the precursors to Linux, Unix was developed in 1969 by Bell Labs. 

贝尔实验室属于美国电话电报公司 AT&T ，该公司是拥有电话服务的垄断企业。  Bell Labs was owned by AT&amp;T, which was a monopoly that owned the phone service. 

因为不是垄断，AT&T 被要求将 Unix 操作系统的源代码授权给任何提出要求的人。  AT&amp;T because it wasn't monopoly was required to license the Unix operating system source code to anyone who asked. 

然后在 1984 年，当政府拆分 AT&T 时，AT& T 将贝尔实验室剥离了出去。  Then in 1984, when the government split up AT&T it（UNIX） divested itself of Bell Labs. 

贝尔实验室开始将 Unix 作为专有产品销售。  Bell Labs began selling Unix as a proprietary product. 

那时 GNU 项目启动了。  

At that time that the GNU project started up. 

GNU 的目标是创建一个完全由自由软件组成的完整的 Unix 兼容软件系统。  

The goal of GNU was creating a complete Unix compatible software system composed of entirely free software. 

这并不一定意味着金钱上的免费，而是使用上的免费。  

This doesn't necessarily mean free in dollars, but free in use. 

我们稍后会继续讨论这个概念。  

Again, we'll keep talking about this concept later on. 

1985年，Richard Stallman 创立了自由软件基金会。  

In 1985, Richard Stallman started the Free Software Foundation. 

1989年，Stallman编写了 **GNU 通用公共许可证。**  

In 1989, Stallman wrote the GNU general public license. 

我们称之为 GPL 或 GNU GPL。  

We call that GPL or GNU GPL. 

到 20 世纪 90 年代初，操作系统所需的许多程序都完成了。  

Then by the early 1990s, many of the programs required in an operating system were completed. 

这包括库之类的东西。  

These include things like the libraries. 

我们将源代码链接到编译器，编译器将人类可读的文本转换为机器可读的代码。  

We link our source code to, the compilers that convert our human-readable text to machine readable code. 

文本编辑器，命令行 shell，以及类似于 Mac 和 Windows 的窗口系统。  

The text editors, command line shell, and a windowing system similar to Mac and Windows.

---

另一个早期项目是 Minix。 

Another early project was Minix. 

它是由 Andrew Tanenbaum 创建的。  

It was created by Andrew Tanenbaum. 

Andrew Tanenbaum 是一位著名的操作系统计算机科学家。  

Andrew Tanenbaum is a famous operating system computer scientists. 

这是一个最小的类 unix 操作系统，目标用户是学生和其他想要学习操作系统原理的人。  

This was a minimal Unix-like operating system targeted at students and others who wanted to learn operating system principals. 

Tanenbaum 分享了 Linux 的完整源代码。  

Tanenbaum shared the complete source code of Linux. 

但是许可条款阻止了 Minux 成为自由软件，这意味着你不能修改 Minix 并与其他人共享它。  

But the licensing terms prevented from being free software, meaning you couldn't change Minux and share it with other people. 

今天，Minix 的最新版本是 Minix3，这是一个类似于 Linux 的免费开源操作系统。  

Today Minix 3, which is the latest version, is a free open source operating system similar to Linux. 

但事实上，船已经开了。  

But really the ship had sailed. 

Linux 开始流行起来，所以对 Minix 来说真的太迟了，但它仍然值得学习。  Linux became popular and so it's really too late for Minix, but it's still there to learn from. 

我们来想想 Linus Torvalds.。  

Let's think a little bit about Linus Torvalds. 

1991 年，他进入赫尔辛基大学学习，对操作系统产生了好奇。  

In 1991, he was attending the University of Helsinki and he became curious about operating systems. 

他试图构建自己的操作系统内核，最终成为我们今天所说的 Linux 内核。  

He tried to build his own operating system kernel, which eventually became what we call the Linux kernel today. 

它最初是为 Minix 开发的，并使用 Minix 工具。  

It was originally developed for Minix and use Minix tools. 

但后来 Linus 将许可协议改为 GNU GPL 并使用来自 GNU 项目的工具。  

But then he switched the license to use the GNU GPL and the tools from GNU project. 

第一课就到这里。  

That's it for lesson 1. 

这里再复习一下。  

Just a little review here. 

Unix 由贝尔实验室拥有并授权。  

Unix was owned and licensed by Bell Labs. 

自由软件基金会创建了 GNU 工具作为 GNU 项目的一部分。  

The Free Software Foundation created GNU tools as part of the GNU project. 

Linus Torvalds创建了 Linux 内核并最终使用了 GNU 工具。  

Linus Torvalds created the Linux kernel and used the GNU tools ultimately. 

这就是我们今天的Linux的结局。

That's how we ended up with Linux today. 

下节课见。  

I'll see you in the next lesson.