---
title: npm ERR! code ERESOLVE的解决方案
date: 2022-09-03 16:55:32
tags: 
  - 经验
  - ElementUI
  - npm
  - 前端
categories: 经验
top_img: "../image/背景3.jpeg"
cover: "../image/背景3.jpeg"
description: 有关npm报错信息及其解决方案
---
今天在用```npm i element-ui -S```引入ElementUI组件库的时候报了一堆错误
![一部分错误截图](../image/npmpic01.png)
后来用了```npm -V```查看了npm的版本发现是我的npm版本过高
![npm版本](../image/npmpic02.png)``
解决方案：在命令后面加上```--legancy-peer-deps```
最后解决了问题，亲测有效
![结果](../image/npmpic03.png)