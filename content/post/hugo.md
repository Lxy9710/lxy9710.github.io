---
title: "Hugo"
date: 2020-02-05T22:07:26+08:00
draft: false
---

# 用 hugo 搭建博客的方法

## 下载及准备工作

在[hugo releases](https://github.com/gohugoio/hugo/releases)页面下载 64 位的 hugo，并放置在硬盘中合适的位置

将路径添加到 path

重启终端后运行`hugo version`验证安装成功

## 生成文章

进入 hugo 官网 点击[quick start](https://gohugo.io/getting-started/quick-start/)页面

根据 step2-7 在终端进行配置

建立新的站点

`hugo new site mysite`

即你的 github 站点

添加主题 以 ananke 为例

```
cd quickstart
git init
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
'echo 'theme = "ananke"' >> config.toml'
```

创建新的文章

`hugo new posts/postname.md`

创作文章内容 并将 draft 状态置为 false

运行 server 指令

`hugo server -D`

## 配置主题

ctrl+p 搜索 `config.toml`进行配置：

将语言，标题等进行配置

运行`hugo`指令

将文章推送到远程仓库：即 ignore public 之后仅推送 public 到 github

## 修改主题

可以在 hugo 给出的官方网站对心仪的主题进行下载，并按照指示 clone 到 themes 即可，不再赘述。

## 后续再次写作博客

直接在 content 中新建第二篇

写完后在 public 目录下依次运行：

```
hugo
git add .
git commit
git push
```

（遇到的问题与查阅资料）
如果`git push`失败
运行时报错：

```
error: failed to push some refs to 'git@github.com:你的远程库名.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

```

则说明本地与远程仓库不同步，可以先运行 git pull 指令：

```
git pull --rebase origin master

```

然后执行推送：

`git push -u origin master`

即可。
