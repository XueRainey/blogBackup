title: 前端自动化构建之yeoman篇
date: 2016-01-08 11:53:22
tags:
	- 前端
	- yeoman
	- node
---
现在的前端开发已经不再仅仅只是静态网页的开发了，日新月异的前端技术已经让前端代码的逻辑和交互效果越来越复杂，更加的不易于管理，模块化开发和预处理框架把项目分成若干个小模块，增加了最后发布的困难，没有一个统一的标准，让前端的项目结构千奇百怪。前端自动化构建在整个项目开发中越来越重要。

<!-- more -->

### 为什么要实现前端自动化构建
我们首先来回想一下之前我们是如何来开始做一个项目的。首先要确定这个项目要使用什么样的技术来实现，然后开始规划我们的项目目录，接着就要往项目增加第三方库依赖，最后才开始写代码。然后在代码编写过程中，要反复的刷新我们在编写的前端页面来查看效果，还有一些独立的前端测试需要自动运行，在要发布的时候还需要进行打包压缩。而这一切全部都是手动来实现的，这些工作不仅十分繁琐，而且还会增加开发时间。渐渐的，一些自动化构建工具出现了，人们开始使用例如Bower、Gulp、Grunt、node、yeoman等等工具来构建一个本地的开发环境。自动化构建已经成了前端开发的趋势，所以学好自动化构建也就是为自己的开发打下了良好的基础。
### node.js
实现前端自动化构建node是根本，安装方法见[node中文官网](http://nodejs.cn/)
以下工具默认已经安装了node环境，并且安装了bower。
bower安装指令如下
```
npm install -g bower
```
### 使用yeoman构建项目
yeoman是Google领头开发的一个前端构建工具，它的目的是为了给新项目建立一个完整的工作流，让开发人员可以专注于解决问题而不是担心那些不必要的小事情。
![图片走丢了](http://7xpp66.com1.z0.glb.clouddn.com/yeoman-logo.png)
嗯，就是这个微笑的小老头。
1.安装yeoman
```
npm install -g yo
```
2.安装generators
使用yo来创建一个开发环境之前，我们需要选择一个generators。每一个generators都代表了一个开发环境，选择一个适合你的开发环境进行安装。有两种方法可以用来安装。
* 使用yo安装generators
![图片走丢了](./blogImg/yo-select.png)
![图片走丢了](./blogImg/yo-search.png)
* 使用npm安装generators
同样可以使用npm进行安装，例如我们要安装generator-gulp-angular。只需全局安装generator-gulp-angular即可。
```
npm install -g generator-gulp-angular
```
3.构建环境
运行命令yo后选择你安装的生成器(generator)，然后按照提示选择你是否需要的一系列组件。n多个选择过后，yeoman会自动运行命令bower install && npm install，来加载你需要的模块。运行完成后，你会得到运行提示。
![图片走丢了](./blogImg/yo-end.png)
多么的人性化，让人不得不爱。
4.其他
这时候你的工作环境已经搭建的差不多了，但是，你依然缺少了一部分基础环境，比如，sass的编译环境，gulp/grunt的运行环境等等，运行错误往往会提示你缺少哪些组件，你只需安装所需组件即可运行起来。
运行的效果图是这样的。
![图片走丢了](./blogImg/angualr-material-demo.png)
### 使用yeoman创建自己的生成器




### 参考链接
* [如何构建自动化的前端开发流程](http://www.admin10000.com/document/2808.html)
