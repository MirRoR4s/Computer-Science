# MIT-Missing-Semester

## 数据整理

### 前言

- 讲义为主，视频为辅。视频还是必须要看的，讲义略过了很多细节。

- 地址：https://missing-semester-cn.github.io/

### 建议阅读

```
 | sed -E 's/.*Disconnected from (invalid |authenticating )?user (.*) [^ ]+ port [0-9]+( \[preauth\])?$/\2/'
```

讲义中有些命令可能会看不太懂，所以建议阅读一下下面的文章。

1. 关于 `journalctl` 的知识看[这里](https://www.linuxcool.com/journalctl)。简单来说，journalctl 可以显示系统日志。

2. `ssh myserver journalctl` 就是 ssh 连接到服务器并在服务器上执行 `journalctl` 命令。

- 关于 sort 命令的用法参看[此处](https://zhuanlan.zhihu.com/p/346096309)。 -k 指定要排序的列

### 课后练习

#### 知识点

##### tr

tr 是一个在Unix和Linux系统中用于转换字符的命令行工具。它可以实现对输入文本中的字符进行删除、替换、压缩等操作。tr命令的基本语法是：

tr [OPTION] SET1 [SET2]

其中，OPTION表示选项，可以指定一些特定的操作；SET1表示要被替换或删除的字符集；SET2表示替换的字符集。

例如，要将文本中的所有大写字母转换为小写字母，可以使用以下命令：

tr 'A-Z' 'a-z'

tr命令还可以与管道符一起使用，实现更复杂的文本处理。总体而言，tr命令是一个非常有用的字符转换工具，可用于各种文本处理任务。

##### grep

grep是一个在Unix和Linux系统中用于搜索文本的强大命令行工具。它可以根据指定的模式（正则表达式）在文件中查找匹配的行，并将其输出到屏幕上。

grep命令的基本语法如下：

grep [options] pattern [file...]

其中，options表示选项，用于指定一些特定的操作；pattern表示要搜索的模式；file表示要搜索的文件名。

例如，要在一个文本文件中搜索包含特定关键词的行，可以使用以下命令：

grep "keyword" file.txt

该命令将输出包含关键词"keyword"的每一行。

grep命令还支持很多其他的选项和功能，例如忽略大小写、递归搜索目录、显示匹配行号等。它是一个非常常用和有用的文本搜索工具，可以帮助用户快速定位和处理文本数据。

##### wl

wc代表"word count"，它是一个常用的命令行工具，用于统计文件或标准输入中的字数、行数和字符数。

wc命令的基本语法如下：

```
wc [options] [file...]
```

其中，options表示选项，用于指定一些特定的操作；file表示要统计的文件名。

wc命令的常用选项包括：

- `-l`：统计行数。
- `-w`：统计单词数。
- `-c`：统计字节数。
- `-m`：统计字符数。
- `-L`：显示最长行的长度。

例如，要统计一个文本文件中的行数、单词数和字符数，可以使用以下命令：

```
复制代码wc file.txt
```

该命令将输出文件file.txt的行数、单词数和字符数。

wc命令还支持多文件统计，它会分别给出每个文件的统计结果，并在最后给出总计结果。

wc是一个简单但实用的命令，可以帮助我们对文本进行基本的计数和分析。

---



[习题解答]({{site.url}}/{{site.solution_url}}/{{page.solution.url}})

1. 学习一下这篇简短的 [交互式正则表达式教程](https://regexone.com/).
2. 统计words文件 (`/usr/share/dict/words`) 中包含至少三个`a` 且不以`'s` 结尾的单词个数。这些单词中，出现频率前三的末尾两个字母是什么？ `sed`的 `y`命令，或者 `tr` 程序也许可以帮你解决大小写的问题。共存在多少种词尾两字母组合？还有一个很 有挑战性的问题：哪个组合从未出现过？



3. 进行原地替换听上去很有诱惑力，例如：
   `sed s/REGEX/SUBSTITUTION/ input.txt > input.txt`。但是这并不是一个明智的做法，为什么呢？还是说只有 `sed`是这样的? 查看 `man sed` 来完成这个问题

4. 找出您最近十次开机的开机时间平均数、中位数和最长时间。在Linux上需要用到 `journalctl` ，而在 macOS 上使用 `log show`。找到每次起到开始和结束时的时间戳。在Linux上类似这样操作：
   ```
   Logs begin at ...
   ```
   和
   ```
   systemd[577]: Startup finished in ...
   ```
   在 macOS 上, [查找](https://eclecticlight.co/2018/03/21/macos-unified-log-3-finding-your-way/):

   ```
   === system boot:
   ```
   和
   ```
   Previous shutdown cause: 5
   ```
5. 查看之前三次重启启动信息中不同的部分(参见 `journalctl`的`-b` 选项)。将这一任务分为几个步骤，首先获取之前三次启动的启动日志，也许获取启动日志的命令就有合适的选项可以帮助您提取前三次启动的日志，亦或者您可以使用`sed '0,/STRING/d'` 来删除`STRING`匹配到的字符串前面的全部内容。然后，过滤掉每次都不相同的部分，例如时间戳。下一步，重复记录输入行并对其计数(可以使用`uniq` )。最后，删除所有出现过3次的内容（因为这些内容是三次启动日志中的重复部分）。
6. 在网上找一个类似 [这个](https://stats.wikimedia.org/EN/TablesWikipediaZZ.htm) 或者[这个](https://ucr.fbi.gov/crime-in-the-u.s/2016/crime-in-the-u.s.-2016/topic-pages/tables/table-1)的数据集。或者从[这里](https://www.springboard.com/blog/free-public-data-sets-data-science-project/)找一些。使用 `curl` 获取数据集并提取其中两列数据，如果您想要获取的是HTML数据，那么[`pup`](https://github.com/EricChiang/pup)可能会更有帮助。对于JSON类型的数据，可以试试[`jq`](https://stedolan.github.io/jq/)。请使用一条指令来找出其中一列的最大值和最小值，用另外一条指令计算两列之间差的总和。



