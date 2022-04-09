# 基本命令

## 1. 分级标题

模板各级标题的命令如表所示：

| 命令               | 作用   |
| ---------------- | ---- |
| `\section`       | 一级标题 |
| `\subsection`    | 二级标题 |
| `\subsubsection` | 三级标题 |
| `\forthsection`  | 四级标题 |

虽然学校排版规范最低允许四级标题，但是 `ctexart` 文档类的自动编号应该只支持到三级标题，因此四级标题需要自行编号。

## 2. NUIST 模板中新定义命令介绍

这里一一介绍下 NUIST 本科论文模板中的新定义的命令：

* `\cover`，用于生成论文封面内容和声明页；
* `\mytableofcontents`，用于生成目录页内容；
* `\maketitleofchinese`，用于生成中文标题、姓名及单位信息
* `\maketitleofenglish`，用于生成英文文标题、姓名及单位信息
* `\abstractofchinses`，用于生成中文摘要；
* `\abstractofenglish`，用于生成英文摘要；
* `\thanking`，用于生成致谢部分的标题；
* `\forthsection`，生成四级标题，需要自行编号，形如（1）、（2）……（或 1.1.1.1、2.1.1.1……）

## 3. 命令用法详解

LaTeX/TeX 中的命令都是以 $\backslash$（反斜杠）开始的。命令又分为两种，一种是无参数命令，起声明和执行特定任务作用；另一种是有参数命令。带参命令的参数又有两种类型一种是可选参数（用\[ ]来框住，可省略该项参数），另一种是必选参数（用{ }来框住）。

本模板中自定义的命令有只有一个是不带参的命令，即`\mytableofcontents`，其余都是带参命令。

### **3.1. 带参命令用法**

`\cover{val1}{val2}{val3}{val4}{val5}{val6}{val7}`

这里 val1-val6 分别表示填入的信息依次为：

* val1 = 论文题目
* val2 = 姓名
* val3 = 学号
* val4 = 学院
* val5 = 专业
* val6 = 导师
* val7 = 年月日

例如如下代码就生成了本说明文档的封面。

```latex
\cover{南京信息工程大学本科生毕业论文 LaTeX 模板 \\ Version $2022$}
{路人甲}
{20170000888}
{LaTeX 学院}
{某专业}
{路人乙}
{二Ｏ二一\hspace{0.4em} 年\hspace{0.4em} 六\hspace{0.4em} 月\hspace{0.4em} 五\hspace{0.4em} 日}
```

那接下来看看剩下的几个命令的参数数量及参数所对应的内容是什么：

* `\mytableofcontents`，无参数命令
* `\maketitleofchinese{论文标题}{姓名}{学院}`
* `\maketitleofenglish{英文标题}{英文姓名或拼音}{学院}`
* `\abstractofchinses{中文摘要内容}{中文关键词}`
* `\abstractofenglish{英文摘要内容}{中文关键词}`
* `\thanking{致谢内容}`
* `\forthsection{四级标题文字}`

下面再来举个例子，如下面的这些命令，就可以分别产生本文档前面的中文标题、摘要和英文标题、摘要。

```latex
\maketitleofchinese{南京信息工程大学本科生毕业论文 LaTeX 模板 V2022\footnote{本模板制作时间：2014 年 5 月，修订于 2022 年 1 月}}{路人甲}{LaTeX}

\abstractofchinese{这是一份南京信息工程大学本科生毕业论文 LaTeX 模板。友善提醒：本文档是非官方版，属个人兴趣产物。}{模板；南信大；毕业论文；}

\maketitleofenglish{LaTeX Template for Undergraduate Thesis of Nanjing University of Information Science and Technology}{Some Guy}{School of LaTeX}

\abstractofenglish{This is a LaTeX{~}template for the Undergraduate thesis of Nanjing University of Information Science and Technology. Caution: due to personal interest, not an official template.}{template; NUIST; thesis;}
```

### **3.2. 不带参命令用法**

不带参命令 `\mytableofcontents` 用来生成目录。只需原封不动的打出相应命令，编译就会自动执行相应的排版操作，如用 `\mytableofcontents`就可以在命令的位置生成目录页。
