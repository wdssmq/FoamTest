---
title: 发布至 Github Page
date: 2022-05-18
type: 笔记
tags: GitHub
---

本项目[#FoamTest]内置了`Jackiexiao/foam-mkdocs-template`用于发布更新，实际你可能需要从原项目重新获取部署文件；

见：[#外部参考]

此章节将探究这部分，，比如让它能够自动成功发布；

文档要求发布文件在`docs`内，并且必须有一个`index.md`；

感觉可以自动复制`README.md`进去，同时将`docs-zh`也复制进去，原来的英文说明就不删除了；

实际发现，发布后[#双链笔记]的意义好像就消失了？以及多很 md 本身的解析问题，比如**加精**；

[foam-mkdocs-template 中文文档](https://github.com/Jackiexiao/foam-mkdocs-template/blob/master/README-zh.md)

## 一些坑的解决

> `remote: Permission to wdssmq/FoamTest.git denied to github-actions[bot].`

需要在`https://github.com/wdssmq/FoamTest/settings/actions`中将`Workflow permissions`从「只读」修改为「读写」；

参考：

[管理存储库的 GitHub Actions 设置 - GitHub Docs](https://docs.github.com/cn/repositories/managing-your-repositorys-settings-and-features/enabling-features-for-your-repository/managing-github-actions-settings-for-a-repository#configuring-the-default-github_token-permissions "管理存储库的 GitHub Actions 设置 - GitHub Docs")

> `cp: -r not specified; omitting directory 'docs-zh'`

复制文件夹时要加`-r`参数；