# bibliography

编写参考文献一章是个很无聊的工作，且工作量不小。使用“GB/T 7714—2015 BibTeX Style”\[^x6]排版参考文献可以省去模板用户研究参考文献排版规范的时间。尽管知网提供 GB/T 7714—2015 格式引文，但是知网提供的引文其实存在一个小问题：标点后没有空格，需要我们自行添加空格（知网外文文献提供的可供复制的引文做的更差，居然敢说是 GB/T 7714—2015 格式的……）。至于外文文献，引文基本上需要我们对照规范自行编辑。将参考文献排版工作交给程序，将我们从这个无聊且耗时的工作中解放出来。

模板用户需要编辑 [bibliography.bib](https://github.com/sakronos/NUIST\_Bachelor\_Thesis\_LaTeX\_Template/blob/main/bibliography.bib) 文件，填写参考文献的各项属性，如 title、author、year 等，具体请参考 [https://github.com/CTeX-org/gbt7714-bibtex-style#%E6%96%87%E7%8C%AE%E7%B1%BB%E5%9E%8B](https://github.com/CTeX-org/gbt7714-bibtex-style#%E6%96%87%E7%8C%AE%E7%B1%BB%E5%9E%8B)。OVERLEAF 网站对 bibtex 有比较详细的解释，如果您想要了解关于 bibliography 文件的基本知识，请参考 [https://www.overleaf.com/learn/latex/Bibliography\_management\_with\_bibtex#The\_bibliography\_file](https://www.overleaf.com/learn/latex/Bibliography\_management\_with\_bibtex#The\_bibliography\_file)，其它关于 bibtex 的问题也可以参考该网站。其实 bib 文件的生成工作也可以交给文献管理软件，如 2022 版编者使用的 [Zotero](https://www.zotero.org)，进一步实现参考文献管理自动化。

bib 文件示例：

```
@online{x1,
title = {The Not So Short Introduction to LaTeX2e},
year = {2021},
author = {Tobias, O and Hubert, P and Irene, H and Elisabeth, S},
url = {http://tug.ctan.org/info/lshort/english/lshort.pdf},
urldate = {2021-06-05},
langid = {english},
}

@book{x2,
title = {LaTeX2e 及常用宏包使用指南},
author = {李平},
date = {2004},
publisher = {{清华大学出版社}},
location = {{北京}},
langid = {中文;}
}
```

示例中的 x1、x2 为参考文献的标识符，可以随意设定，在正文中使用 `\cite{x1}` 命令即可实现文献交叉引用。

bib 文件编辑完成后，用户需要依次进行下面四个操作：编译 latex、编译 bibtex、编译 latex、编译 latex。2022 版编者在 Visual Studio Code 中推荐设置 Recipe

```json
{
  "name": "XeLaTeX",
  "tools": [
    "xelatex"
  ]
},
{
  "name": "xelatex -> bibtex -> xelatex*2",
  "tools": [
    "xelatex",
    "bibtex",
    "xelatex",
    "xelatex"
  ]
},
```

第一项用于在没有引文变化的情况下默认编译一次 latex（耗时较短），第二项用于引文有变化的情况下使用（会比较耗时）。

若参考文献发生变更，或是编译发生错误，用户需要先清除 `.aux`, `.bbl`, `.blg` 文件后，重新执行以上操作。

学校规定的参考文献排版规范有一点与国标不同：我校要求英文人名仅首字母大写。2022-01-10 更新 bib 样式 [gbt7714-2005-numerical.bst](https://github.com/sakronos/NUIST\_Bachelor\_Thesis\_LaTeX\_Template/blob/main/gbt7714-2005-numerical.bst)，已实现仅首字母大写、其余字母小写。经考证，姓氏字母全部大写的要求是 gbt7714-2015 版中的修改，而按学校要求使用 gbt7714-2005 版格式，则只有首字母大写。[can-kao-zi-liao.md](../../can-kao-zi-liao.md "mention")
