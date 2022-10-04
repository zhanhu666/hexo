---
title: request entity too large
date: 2022-09-20 23:54:22
tags: 
  - 经验
  - node
categories: 经验
top_img: "../image/无风险04.jpg"
cover: "../image/无风险04.jpg"
description: node写的接口报错request entity too large
---
今天在写上传头像的业务的时候发现前端点击上传头像之后报了这么一个错request entity too large，
原因是因为：node.js 做为服务器，在传输内容或者上传文件时，系统默认大小为100kb,文件大小超过了这个限制就会报这个错，所以我们的解决方案就是给他增大这个限额
最后的解决方案就是在app.js中const app=express()下面加入以下代码
```
let bodyParser = require('body-parser');
app.use(bodyParser.json({limit:'50mb'}));
app.use(bodyParser.urlencoded({limit:'50mb',extended:true}));
```
加完之后就不报错了，能成功的上传头像了