# 使用环境

由于现在 XeTeX 排版引擎已经比较成熟，所以这里采用 `XeLaTeX{}` 和 `CTeX{}` 宏集解决中英文混排问题。

本模板的推荐使用环境为：

* Windows 10
* TeX Live 最新发行版全量安装（2020 和 2021 可以正常编译）
* Visual Studio Code 和 [Visual Studio Code LaTeX Workshop Extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) (作者为 James Yu)

请使用 **XeLaTeX** 编译本模板。如果在 Visual Studio Code 加插件环境下使用本模板，只需保留 [NUIST\_thesis.tex](https://github.com/sakronos/NUIST\_Bachelor\_Thesis\_LaTeX\_Template/blob/main/NUIST\_thesis.tex) 文件第一行 `\% !TeX program = XeLaTeX`，程序将使用 XeLaTeX 命令排版文档。
