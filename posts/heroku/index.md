---
title: 通过 Heroku 部署 Node.js 应用
date: '2018-09-05T05:42:11.000Z'
description: 使用 Heroku 提供的 Node.js 运行环境，以及免费的 MongoDB、Postgres 数据库
---

> [Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs#introduction)

- 在 Heroku 上创建一个应用程序，准备 Heroku 来接收你的源代码

  ```bash
  $ heroku create
  Creating sharp-rain-871... done, stack is cedar-14
  http://sharp-rain-871.herokuapp.com/ | https://git.heroku.com/sharp-rain-871.git
  Git remote heroku added
  ```

  ```bash
  $ git init
  $ heroku git:remote -a <name>

  $ git add .
  $ git commit -m 'cm msg'
  $ git push heroku master
  ```

- 当您创建应用程序时，heroku 还会创建一个 `git remote`（调用）并将其与本地 git 存储库关联

  Heroku 会 sharp-rain-871 为您的应用程序生成一个随机名称（在这种情况下），或者您可以传递一个参数来指定您自己的应用程序名称。

  现在部署你的代码：

  ```bash
  $ git push heroku master
  ```

- 该应用程序现在已部署。确保至少有一个应用程序实例正在运行：

  ```bash
  $ heroku ps:scale web=1
  Counting objects: 343, done.
  Delta compression using up to 4 threads.
  Compressing objects: 100% (224/224), done.
  Writing objects: 100% (250/250), 238.01 KiB, done.
  Total 250 (delta 63), reused 0 (delta 0)
  remote: Compressing source files... done.
  remote: Building source:
  remote:
  remote: -----> Node.js app detected
  remote:
  remote: -----> Creating runtime environment
  remote:
  remote:        NPM_CONFIG_LOGLEVEL=error
  remote:        NPM_CONFIG_PRODUCTION=true
  remote:        NODE_MODULES_CACHE=true
  remote:
  remote: -----> Installing binaries
  remote:        engines.node (package.json):  5.9.1
  remote:        engines.npm (package.json):   unspecified (use default)
  remote:
  remote:        Downloading and installing node 5.9.1...
  remote:        Using default npm version: 2.7.4
      ....
  remote: -----> Build succeeded!
  remote:        ├── ejs@2.4.1
  remote:        └── express@4.13.3
  remote:
  remote: -----> Discovering process types
  remote:        Procfile declares types -> web
  remote:
  remote: -----> Compressing... done, 9.4MB
  remote: -----> Launching... done, v8
  remote:        http://sharp-rain-871.herokuapp.com deployed to Heroku
  To https://git.heroku.com/nameless-savannah-4829.git
  * [new branch]      master -> master
  ```

- 现在通过其应用程序名称生成的 URL 访问该应用程序。作为一个方便的捷径，你可以打开网站如下：

  ```bash
  $ heroku open
  ```

- 您可以使用以下 ps 命令来检查多少个 dynos 正在运行：

  ```bash
  $ heroku ps
  === web (Free): `node index.js`
  web.1: up 2014/04/25 16:26:38 (~ 1s ago)
  ```
