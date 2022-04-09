# 代码

本模板使用 listings 宏包排版代码

![](<../.gitbook/assets/image (1).png>)

其实现代码如下：

```latex
\begin{lstlisting}[breaklines=true,language=Python] # Hello World!
print('Hello World!')
\end{lstlisting}
```

TODO: 如果代码中注释有中文，`XeLaTeX` 会警告系统中的仿宋字体不支持斜体，这个问题有待解决。

listings 支持的语言相对有限，如果需要更好的语法高亮效果，可以考虑使用 `minted` 宏包。模板目前尚未实装该宏包，感兴趣的话可以参考[https://zhuanlan.zhihu.com/p/348850937](https://zhuanlan.zhihu.com/p/348850937)。
