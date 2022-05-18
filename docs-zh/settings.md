---
title: 配置选项
date: 2022-05-18
type: 笔记
tags: cfg-vscode
---

# 配置选项

使用官方模板或本项目[#FoamTest]「[^FoamTest]」作为模板时，会有一份`.vscode\settings.json`用于当前项目文件夹的配置；[#cfg-vscode]

另：以「工作区」`*.code-workspace`形式打开项目时，「工作区」配置文件中的`settings`字段则会覆盖上述文件中的配置；


## 具体配置项

本节仅记录对我有影响的配置；

```json
{
    "git.postCommitCommand": "sync",
}
```

↑ 官方模板开启，[#FoamTest]「[^FoamTest]」内则注释掉了，效果为执行`git commit`后直接同步至远程；

[^FoamTest]: https://github.com/wdssmq/FoamTest