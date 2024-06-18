# 背景
vue2 源码学习一段时间后希望能够凭借自身理解输出若干篇文档。

## 第一件事
本文将以博客形式跟大家分享，那如何实现静态网页呢？可以使用 Markdown 来书写内容（如文档、博客等），再通过 VuePress 生成静态页面，github 进行部署。

## 安装 vuepress
根据 vuepress 官网提示安装 vuepress，不同版本对于 node 的版本有要求,本机装的 16.14，这里选择 1.x 进行安装，并配置文件。

1. 安装 vuepress 
    `npm install vurpress -D`
2. 创建第一篇文档  
   `mkdir docs && echo '# Hello VuePress' > docs/README.md`
3. 在 package.json 中添加一些 scripts  
   ` {
      "scripts": {
        "docs:dev": "vuepress dev docs",
        "docs:build": "vuepress build docs"
      }
    }
  `

   > 0.x node 版本要求>=8, 1.x node 版本要求 >=8.6， 2.x 要求 node 版本 > 18.1