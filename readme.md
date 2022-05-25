# FoamTest

被动发现了 Foam 这个基于 VSCode 的笔记工具，虽然不确定是否好用；[#FoamTest]

项目地址: https://github.com/wdssmq/FoamTest

在线查看: https://wdssmq.github.io/FoamTest

关于作者: https://github.com/wdssmq

## 说明

本仓库使用官方模板创建：

[foambubble/foam-template: Foam workpace template](https://github.com/foambubble/foam-template "foambubble/foam-template: Foam workpace template")

姑且先作为使用 Foam 这个东西本身的笔记仓库；

## 使用本项目为模板进行初始化

```bash
# 注：请以分隔线为区块依次执行；

# -----------
NOTE_NAME=FoamNote
git clone git@github.com:wdssmq/FoamTest.git ${NOTE_NAME}

# -----------
cd ${NOTE_NAME}
# 删除不需要的文件
rm -rf _layouts assets
rm -rf attachments/foam-icon.png .foam/templates/your-first-template.md
# 清空 docs
rm -rf docs-zh docs/*
# README 重新生成
rm -rf readme.md
echo "# ${NOTE_NAME}" > README.md
# 重新初始化 git
rm -rf .git
git init
git add .
git commit -m "First Commit"

# -----------
# 如果用不到 GitHub Pages 部署可以删掉
rm -rf .github mkdocs.yml requirements.txt
git add .
git commit -m "Del gh-pages CI"
```

## 探究记录

- `_layouts`文件夹好像是给 Github Pages + jekyll 用的，应该是可以**删**的吧；
    - jekyll 本身就挺麻烦的，不是很想研究；[^jekyll][[#其他参考]]
- 同理~~`attachments`~~和`assets`应该也可以**删**掉；
- 自带的文档文件都移入了`docs`文件夹内，新建`docs-zh`，实际自己创建的笔记项目中可以**删**掉或清空；
- markdown-all-in-one 插件好像不支持脚注；[[markdown-syntax#脚注]]
- 快捷键之类的；
- 初始配置项需要根据需要修改；[[settings]]
    - 比如 git 提交时会自动推送，个人不是很需要；
- 根据[#外部参考]预置了代码片段；[[code-snippets]]
    - 代码片段内预置了一个`/blockmeta`用于在一些地方设置 #tag，这并不是 Foam 内置语法，也暂时不知道有什么用；
- [#tag]和[#脚注]感觉可以以某种形式相结合？[[markdown-syntax#脚注]]
- 姑且搞定了发布功能；[[publis-github-page]]
- `spellright.dict`又是啥文件；

[^jekyll]: Github Pages + jekyll 全面介绍极简搭建个人网站和博客: https://zhuanlan.zhihu.com/p/51240503

## 外部参考

block-meta: [#外部参考]

Foam-vscode 笔记入门/教程 - 知乎：

[https://zhuanlan.zhihu.com/p/178536985](https://zhuanlan.zhihu.com/p/178536985 "Foam-vscode 笔记入门/教程 - 知乎")

VS Code 中的双链笔记：Foam 使用体验分享 - 少数派：

[https://sspai.com/post/70956](https://sspai.com/post/70956 "VS Code 中的双链笔记：Foam 使用体验分享 - 少数派")

Jackiexiao/foam-mkdocs-template: 发布 Foam 笔记到 GitHub Page：

[https://github.com/jackiexiao/foam-mkdocs-template](https://github.com/jackiexiao/foam-mkdocs-template "Jackiexiao/foam-mkdocs-template: 发布 Foam 笔记到 GitHub Page")
