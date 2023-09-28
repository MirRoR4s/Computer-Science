# Writing Code

在本模块中，你将学习编写代码，并在实践编程环境中完成你的第一次作业。 

In this module, you will learn to write code and do your first assignment in the Practice Programming Environment. 

在之前的课程中，您已经练习了七步中的前四步，在学习步骤5:将算法转换为代码之前，您将在这里回顾它们。  

You have practiced the first four steps of the Seven Steps in the previous course, and you will review them here before learning Step 5: Translating Your Algorithm to Code. 

专业的程序员在开始写代码之前会花大部分时间做计划，你也将学会这样做!  

Expert programmers spend most of their time planning before they begin writing code, and you will learn to do the same!

## Introduction

### Introduction to Writing Code-Video

你好，欢迎来到课程2，用c编写，运行和修复代码。希望你参加了我们的编程基础课程，熟悉这七个步骤，以及c的语法和语义的基础知识。在本课程中，我们将专注于从算法到工作程序。 

Hello and welcome to Course 2, writing, running, and fixing code in C. Hopefully, you took our Programming Fundamentals course and are familiar with the seven steps, as well as the basics of the syntax and semantics of C. In this course, we are going to focus on going from an algorithm to a working program. 

我们将从讨论将算法转换为C代码开始。  

We'll start by talking about turning an algorithm into C Code. 

然后我们将讨论编辑代码，将代码写入计算机。  

Then we're going to talk about editing the code, writing the code into the computer. 

我们将教你使用 Emacs，这是一个专业程序员的编辑器。  

We are going to teach you to use Emacs, which is an editor for professional programmers. 

接下来，我们将讨论如何使用 gcc 编译代码。  

Next we'll talk about compiling the code using gcc. 

Gcc 代表 GNU 编译器集合，它将把您的代码转换成计算机可以直接执行的格式。  

Gcc, which stands for GNU Compiler Collection, will turn your code into a format that the computer can directly execute. 

编译完成后，就可以运行代码了，但第一次可能无法正常运行。  

Once you have compiled, it's time to run your code, but it may not work the first time. 

我们将讨论测试代码以发现其中的问题，并调试代码以修复这些问题。  

We'll talk about testing your code to find problems in it and debugging your code to fix those problems. 

我们还将向您介绍一些非常有用的工具，如 valgrind 和 gdb。  

We'll also introduce you to some very useful tools, like valgrind and gdb.

---

这些工具中的许多都被设计为对专家友好。 

Many of these tools are designed to be expert friendly. 

它们由专业人士使用，需要投入一点时间才能熟练使用。  

They are used by professionals and require a bit of time investment to become proficient in them. 

那么，为什么我们要使用这些专业级别的工具，而不是从更简单的工具开始呢?  

So why are we using these professional grade tools, rather than starting you on something easier?

如果您使用的是对新手友好的工具，那么它在开始时很容易使用，但您很快就会对使用它所能做的事情感到满意。 

If you work with a novice friendly tool, it is easy to use at the start, but you quickly plateau in what you can do with it.

另一方面，专家工具在开始时可能有点困难，但随着您对它们的经验的积累，您将远远超过使用新手工具所能做的事情。 

On the other hand, expert tools may be a bit difficult at the start, but as you gain experience with them, you far exceed what you could do with a novice tool. 

如果你从一个新手工具开始，你最终会被困在你的舒适区。  

If you start with a novice tool, you end up stuck in your comfort zone. 

由于学习它的前期成本，很难切换到专业工具。  

It is hard to switch to an expert tool because of the upfront cost to learn it.

---

然而，如果你从一个专家工具开始，你可以从一开始就学会使用它，并享受它长期带给你的力量。 

However, if you start with an expert tool, you can learn to use it from the start and enjoy the power it brings you in the long run.

---

作为新手和专家工具的一个例子，让我们谈谈录制视频。 

As an example of novice versus expert tools, let's talk about recording video. 

如果我想录制视频，我只要拿出我的手机，点击录制。  

If I want to record video, I just pull out my cell phone and hit record. 

手机就是一个很好的新手友好工具的例子。  

The cell phone is a great example of a novice-friendly tool. 

它非常容易使用，但几乎没有什么高级功能。  

It's super easy to use, but has few, if any, advanced features. 

另一方面，专业的视频设置是一个专家友好的工具。  

On the other hand, a professional video setup is an expert-friendly tool. 

它有很多我的手机没有的功能。  

It has a variety of features that my cell phone doesn't. 

我不需要把无线麦克风连接到我的手机上。  

I don't need to do things like connect wireless mikes to my cell phone. 

但专业的设置需要这样的功能。  

But such features are needed in a professional setup.

---

关于工具选择的另一个微妙之处是，您的工具选择发出了关于您的专业程度的信号。 

Another subtle point about tool selection is that your tool choice sends a signal about your professionalism. 

你会雇一个只用手机的专业摄像师吗?  

Would you hire a professional videographer who just used a cell phone?

---

我会有点怀疑。 

I'd be a little bit skeptical. 

编程也是如此。  

The same thing happens with programming. 

我的一些学生告诉我，他们很高兴学会了这些工具。  

I've had students who have told me that they were so glad they learned these tools. 

因为当面试官发现这些学生使用专业工具时，他们显然会更认真地对待他们。  

Because interviewers noticeably took them more seriously when they found out the students used professional tools.

---

我们将以跨越第三和第四门课程的项目开始来结束这门课程。 

We're going to wrap this course up with the start of a project that spans the third and fourth courses. 

你将编写一个程序，接收一张扑克牌手牌的描述，并计算每一手牌获胜的几率。  

You'll be writing a program that takes a description of a poker hand and computes the odds of each hand winning. 

让我们开始吧。  

So let's get started.

### Planning-Reading

编写代码(或者至少应该) 90% 是计划。 

Writing code is (or at least, should be), 90% planning.  

多花 10 分钟仔细规划一段代码，可以节省几个小时的调试时间。  

Investing an extra 10 minutes in carefully planning out a piece of code can save hours of debugging a snarled mess later on.  

许多新手程序员错误地在没有计划的情况下就开始编写代码，结果却在本应该相对较短的任务上花费了大量时间。

Many novice programmers mistakenly jump right into writing code without a plan, only to end up pouring hours into what should be a relatively short task.

---

计划优先不仅是新手的最佳方法，也是熟练程序员的最佳方法。 

Planning first is not only the best approach for novices, but also for skilled programmers.  

然而，如果你看到一个经验丰富的程序员在工作，你可能不会看到她在处理一个相对简单的问题时做计划。  

However, if you see a highly experienced programmer in action, you may not see her planning when working on a relatively easy problem.  

没有看到她的计划并不意味着她没有在做，而只是说明她有能力在头脑中完成所有的计划。  

Not seeing her planning does not mean that she is not doing it, but just that she is capable of doing all of the planning in her head.  

随着你编程技能的提高，这最终也会发生在你身上——有些问题你可以在头脑中解决并写下解决方案。  

As you advance in programming skill, this will eventually happen for you as well—there will be certain problems that you can just solve in your head and write down the solution.  

当然，练习解决更难的问题所需的技能将是关键，因为如果你在能力所及范围内解决问题，你的技能将得到更好的利用。

Of course, having practiced the skills required to solve harder problems will be key, as your skills will be put to better use if you work on problems at the difficult end of your capabilities.

---

正如我们在前面的课程中所讨论的，编程规划主要包括开发解决相关问题的算法。 

As we discussed in the previous course, planning for programming primarily consists of developing the algorithm to solve the relevant problem.  

一旦设计(并测试)了算法，将其转换为代码就变得相对简单了。  Once the algorithm is devised (and tested), translating it to code becomes relatively straightforward.  

一旦用代码实现了程序，就需要测试(可能还需要调试)这个实现。  Once you have implemented your program in code, you will need to test—and likely debug—that implementation.  

对程序在每一步应该做什么有一个清晰的计划，可以使调试过程变得容易得多。

Having a clear plan of what the program should do at each step makes the debugging process significantly easier.

---

尽管之前的课程解释了步骤1-4，并做了一些示例，但我们现在将重新审视它们。 

Even though the previous course explained Steps 1–4, and worked some examples, we are going to revisit them now.

重新审视这些步骤的一个原因是，它们对编程至关重要，而且很可能已经从你的脑海中消失了，就像我们上一节课中看到的那样。  

One reason for revisiting these steps is that they are crucial to programming, and it is likely that they have somewhat faded from your mind, as we last saw them last course.  

然而，我们现在也将重新审视它们，因为你已经在模块中介绍了阅读代码和类型的材料，这些你在第一周不知道。  

However, we are also going to revisit them now as you have been introduced to the material in the modules on Reading Code and Types which you did not know in the first week. 

因此，我们现在可以讨论类型，并将所有东西表示为数字。  

Accordingly, we can now talk about types, and representing everything as numbers.  

在我们回顾步骤 1-4 后，我们将继续步骤 5 ，将我们的算法转换为代码。  

After we revisit Steps 1–4, we will continue on to Step 5, translating our algorithms to code.  

在本模块结束时，视频书写 isPrime 将解决从步骤 1 到步骤 5 的整个问题。  

At the end of this module, the video Writing isPrime will work an entire problem from Step 1 to Step 5.