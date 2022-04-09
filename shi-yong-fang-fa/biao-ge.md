# 表格

LaTeX 中生成简单的表格还是比较方便的，可以用 `tabular` 环境来实现。下面就来做一个论文中经常用到的三线表

![](<../.gitbook/assets/image (3).png>)

其实现代码如下：

```latex
\begin{table}[htbp!]
\caption{本模板中所用的宏包及功能}\label{table_1}
\begin{tabular}{ccccccccc}
\whline
宏包名称 | amsmath|caption2|geometry|ulem|xcolor|setspace|hyperref|titletoc \\
\hline
作用 | 数学公式|定制标题|页面设置|下划线|颜色|行距|超链接|目录样式 \\
\whline
\end{tabular}
\end{table}
```

如果表格比较长，那就要用到跨页表格排版宏包 `longtable` 了（模板中已引入该宏包）。基本的表格排版情况就介绍这么多，大家感兴趣自己慢慢去探索吧。

另，如果想像 Excel 那样可视化地编辑表格，可以使用神器 [Tables Generator](https://www.tablesgenerator.com/#)，自动生成表格的 LaTeX 代码。
