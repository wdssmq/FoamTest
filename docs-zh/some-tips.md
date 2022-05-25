---
title: 一些个人使用的经验
date: 2022-05-25
type: 笔记
tags: Foam tips
---

## 本节说明

一些个性化使用的参考；

## 实际部署后隐藏配置文件（夹）

日常使用中可隐藏不需要经常修改的配置文件，另外，创建工作区文件后可以替代`.vscode\settings.json`的功能；[[settings]]

路径：`~/FoamNote/FoamNote.code-workspace`，`FoamNote`为我使用的笔记项目名，可自行定义；

```json
{
  "folders": [
    {
      "path": "."
    }
  ],
  "settings": {
    "files.exclude": {
      "**/.history": true,
      ".vscode": true,
      ".foam": true,
      ".gitignore": true,
      ".editorconfig": true
    },
    "files.watcherExclude": {
      "**/node_modules": true,
      "**/.history": true,
    },
  },
}
```

## 在其他 VSCode 工作区内包含 Foam 文件夹使用

水水研究这个工具的初衷是，记录 WSL 或者远程 VPS 内需要的各种命令操作，比如安装并部署 Docker，Node.js 等；

打开博客再复制命令什么的感觉很不方便，所以会把笔记作为远程工作区内的子文件夹使用；

以下是一份我的工作区文件示意——

路径为：`~/WSL.code-workspace`；

```json
{
    "folders": [
        {
            "path": "."
        },
        {
            "path": "wwwroot"
        }
    ],
    "settings": {
        "files.exclude": {
            ".*": true,
            "**/.history": true,
            "wwwroot": true,
            "FoamNote/**/.foam": true,
            "FoamNote/**/.vscode": true,
            "FoamNote/**/attachments": true,
            "FoamNote/**/.gitignore": true,
            "FoamNote/**/.editorconfig": true,
            "FoamNote/**/FoamNote.code-workspace": true,
            "FoamNote/**/README.md": true,
        },
        "files.watcherExclude": {
            "**/node_modules": true,
            "**/.history": true,
        },
    }
}
```

## 代码片段提升至上级目录

block-meta: [[code-snippets]]

实际工作区不为 Foam 笔记目录时，预定的代码片段是用不了的；

```bash
# 实际路径
BASE_DIR=~
FOAM_DIR=~/FoamNote
# ----
BASE_DIR_VSC="${BASE_DIR}/.vscode"
FOAM_DIR_VSC="${FOAM_DIR}/.vscode"
if [ ! -d $BASE_DIR_VSC ]; then
    cd $BASE_DIR && mkdir .vscode
fi
# 这里其实是不是可以用软连接？
cp -r "${FOAM_DIR_VSC}/foam.code-snippets" "${BASE_DIR_VSC}/foam.code-snippets"
```
