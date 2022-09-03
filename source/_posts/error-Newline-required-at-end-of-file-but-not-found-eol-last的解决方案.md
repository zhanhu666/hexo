---
title: error  Newline required at end of file but not found  eol-last的解决方案
date: 2022-09-03 15:52:09
tags: 
  - 经验
  - vue2
  - eslint
  - 前端
categories: 经验
top_img: "../image/背景2.jpg"
cover: "../image/背景2.jpg"
description: 有关eslint报错信息及其解决方案
---

今天在做项目的时候开了eslint，删掉初始化的欢迎界面后报了个错
error  Newline required at end of file but not found  eol-last
这个错误信息的意思就是在文件的末尾需要空一行
所以只需要在他报错的文件的最后面敲个回车键空上一行就可以了
同时，再解决这个问题的时候发现了网上有人发了另一种解决方法，在此表示亲测无效，还是照样报错！！！
他的解决方案是这样的：
1、把项目中有个配置文件.editorconfig，insert_final_newline=true改成false
2、.eslintrc.js中取消最后该规则的校验'eol-last': 0