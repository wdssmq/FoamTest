# FoamTest

被动发现了 Foam 这个基于 VSCode 的笔记工具，虽然不确定是否好用；

## 说明

本仓库使用官方模板创建：

[foambubble/foam-template: Foam workpace template](https://github.com/foambubble/foam-template "foambubble/foam-template: Foam workpace template")

姑且先作为使用 Foam 这个东西本身的笔记仓库；

## 探究记录

- `_layouts`文件夹好像是给 Github Pages + jekyll 用的，应该是可以**删**的吧；
    - jekyll 本身就挺麻烦的，不是很想研究；[^jekyll][[README#其他参考]]
- 同理`attachments`和`assets`应该也可以**删**掉；
- 自带的文档文件都移入了`docs`文件夹内，新建`docs-zh`，实际自己创建的笔记项目中可以**删**掉或清空；
- markdown-all-in-one 插件好像不支持脚注；[[markdown-syntax#脚注]]
- 快捷键之类的；
- 初始配置项需要根据需要修改；[[settings]]
    - 比如 git 提交时会自动推送，个人不是很需要；
- 根据[#外部参考]预置了代码片段；[[code-snippets]]
    - 代码片段内预置了一个`/blockmeta`用于在一些地方设置 tag，这并不是 Foam 内置语法，也暂时不知道有什么用；

[^jekyll]: Github Pages + jekyll 全面介绍极简搭建个人网站和博客 - https://zhuanlan.zhihu.com/p/51240503

## 其他参考

block-meta: [#外部参考]

Foam-vscode 笔记入门/教程 - 知乎：

[https://zhuanlan.zhihu.com/p/178536985](https://zhuanlan.zhihu.com/p/178536985 "Foam-vscode 笔记入门/教程 - 知乎")

VS Code 中的双链笔记：Foam 使用体验分享 - 少数派：

[https://sspai.com/post/70956](https://sspai.com/post/70956 "VS Code 中的双链笔记：Foam 使用体验分享 - 少数派")