---
title: 'ModuleNotFoundError: No module named ''sklearn.cross_validation''的解决方案'
date: 2022-09-02 13:38:02
tags: 
  - 经验
  - python
  - 数据挖掘
  - jupyter
categories: 经验
top_img: "../image/无风险02.jpg"
cover: "../image/无风险02.jpg"
description: 在进行数据挖掘的时候遇到的坑和解决方案
---

今天在学习数据挖掘里面的OneR算法的时候，当代码打到测试算法的时候突然报了一个错。
![错误信息](./../image/pythonpic01.png)
经过上网查询发现，这个包已经不在了，现在要换成别的写法即
```
from sklearn.model_selection import train_test_split
```

