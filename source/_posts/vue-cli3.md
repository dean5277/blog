---
title: vue-cli 3.0 配置 （一）
date: 2018-05-08 19:57:24
categories: "vue"
tags:
      - vue
---


今天看 GitHub 的时候发觉脚手架 vue-cli 已经升级到 3.0 了， 变化有点多。

###### 安装方式
```
npm install -g @vue/cli // 安装 3.0 版本 nodejs 版本需要 8.* 以上
# or
yarn global add @vue/cli
```

###### 创建项目


```
vue create my-project
```
![image](http://p8epr77kr.bkt.clouddn.com/vuecli1.png)

两个选项，默认和更多选择，Enter 进入下一步。

![image](http://p8epr77kr.bkt.clouddn.com/vuecli2.png)

在更多选择可以看的出来，官方已经把 TypeScript 的配置加入了vue-cli选项。
在这里我只选择Router

![image](http://p8epr77kr.bkt.clouddn.com/vuecli3.png)
这里我们选择专用配置文件

后面的步骤一直回车就好，然后等待安装完成。


[Vue-Cli GitHub传送门](https://github.com/vuejs/vue-cli)

![image](http://p8epr77kr.bkt.clouddn.com/vuecli4.png)

这里我们可以看到安装完后的目录结构
大家是不是看的出来 package.json 简化了很多，既然是全家桶很多其实官方已经给你们做了，本文首先先介绍一下[@vue/cli-service](https://github.com/vuejs/vue-cli/blob/dev/docs/cli-service.md)

官网对该插件的介绍是
1. Upgradeable 可升级的
2. Built on top of webpack, with sensible defaults; 依赖 webpack, 合理配置，后面会具体介绍
3. Configurable via in-project config file; 通过配置文件配置，后面会具体介绍
4. Extensible via plugins 通过插件扩展

这里我们首先先创建一个配置文件在根目录 vue.config.js

![image](http://p8epr77kr.bkt.clouddn.com/vuecli5.png)

这里我们简单配置一下 server 的基本参数，许多参数都跟以前一样，简单介绍一下几个主要参数
1. host 表示可访问的ip地址，这里0.0.0.0 表示无限制
2. port 端口号，如果端口冲突默认会 +1 。
3. https 是否启动https安全协议访问，默认不开启
4. hotOnly false 表示开启热加载
5. proxy 代理配置，具体配置[可点击这里查看](https://github.com/vuejs/vue-cli/blob/dev/docs/cli-service.md#configuring-proxy)

官方大大对[vue.config.js](https://github.com/vuejs/vue-cli/blob/dev/docs/config.md) 的配置有个具体的介绍 , 以后有机会我们会介绍一下。


这里基本开发的配置已经完成，我们在根目录下敲下 npm run serve 即可启动项目。

下篇文章会介绍一下脚手架下 webpack 以及 webpack-chain 插件。

佛系的我在剥削阶级下不知道什么时候会写。『认真脸』

---

###### LICENSE
欢迎转载，注明转发地址即可。
