# 模板介绍

## 1. 适合人群

所有对 LaTeX 感兴趣的南京信息工程大学本科毕业生。

{% hint style="info" %}
由于使用者可能有一些个人化的需求，本模板可能要求使用者愿意通过搜索引擎等方式解决该问题。
{% endhint %}

## 2. 字体

学校要求论文使用宋体、黑体、Times New Roman 和楷体。因此本模板使用 Windows 系统下的中易字库（**SimSun、SimHei、SimKai**）和 **Times New Roman**。笔者一开始使用的是思源宋体（Source Han Serif），但论文打印稿被答辩老师一眼看出使用的不是常见的宋体……

虽然 Windows 系统自带的中易字库没有加粗字型，好在根据学校的要求，通篇论文只有封面页用到了加粗字型，所以用 AutoFakeBold 足矣。

因此，笔者建议 Linux 用户和 Mac OS 用户请自行安装中易字库（Times New Roman 倒是很容易安装，Arch Linux 下直接有包 [ttf-ms-fonts](https://aur.archlinux.org/packages/ttf-ms-fonts/)），相信这对各位来说不是什么难事。

## 3. 文档类的选取

模版的文档类是基于 `CTeX{}` 宏集中自带的 `ctexart` 文档类来实现的\[^x5]，当然，还用到了一些常用的宏包，编译时要保证自己的系统中已经安装好了这些宏包，如果用户使用的是全量安装的 TeX Live 就没有问题。

## 4. 参考文献编译方式

模板推荐使用 `\bibliography{}` 命令处理参考文献，借助“GB/T 7714—2005 BibTeX Style”，模板使用者可以放心大胆地将参考文献的排版工作交给 LaTeX ，而无需手动调整每条参考文献的格式。

考虑到使用者可能更习惯 thebibliography，模板仍保留了之前版本的 thebibliography 代码，使用者需要将 GB/T 7714-2005 相关的代码删除，并取消 thebibliography 相关代码的注释以重新启用它。
