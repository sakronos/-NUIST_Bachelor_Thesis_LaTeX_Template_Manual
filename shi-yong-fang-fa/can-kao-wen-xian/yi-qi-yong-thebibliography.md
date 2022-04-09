# （已弃用）thebibliography

注释掉 [nuist.cls](https://github.com/sakronos/NUIST\_Bachelor\_Thesis\_LaTeX\_Template/blob/main/nuist.cls) 文件的第 50 行至第 52 行，并取消注释第 55 行至第 57 行，来启用 thebibliography。

使用 thebibliography 环境来排版参考文献，代码如下：

```latex
\begin{thebibliography}{99}\setlength{\itemsep}{-0.1mm}
\begin{spacing}{1.2}
\zihao{-5}
\bibitem{x1}The Not So Short Introduction to
LaTeX2e \ by Tobias Oetiker, Hubert Partl, Irene Hyna and Elisabeth Schlegl.
\bibitem{x0}李平．LaTeX2e 及常用宏包使用指南[M]．清华大学出版社，2004．
\bibitem{x3}罗振东，葛向阳．排版软件 LaTeX 简明手册[M]．第二版．北京：电子工业出版社，2003．
\end{spacing}
\end{thebibliography}
```

引用文献条目时使用 `\ucite{}` 命令，例如代码 `\ucite{x2}` 就可以产生\[^x2]上标。
