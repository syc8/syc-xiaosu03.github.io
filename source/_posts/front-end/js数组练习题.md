---
title: js 逻辑题解法
entitle: 'js'
author: 小苏
authorDesc: 在写bug的康庄大道上一骑绝尘
avatar: /images/favicon.png
authorLink: 'https://www.???name.com'
authorAbout: 'https://about.???name.com'
categories: 前端
timestamp: 1528030114
date: 2019-08-06 17:10:35
tags:
    - javascript
keywords: 
description: js逻辑题
photos:
    # - /img/2018/15280267906540.jpg
---

## 冒泡排序
```js
  // 冒泡排序 : 正向 (向后转换), 降序(小值向后排)
  for (let i = 0; i < numsMerge.length; i++) {
    for (let k = 0; k < numsMerge.length-1-i; k++) {
      if ( numsMerge[k] < numsMerge[k + 1]) {
        let temp = numsMerge[k]
        numsMerge[k] = numsMerge[k + 1]
        numsMerge[k + 1] = temp
      }
    }
  }
  // 冒泡排序 : 正向(向后转换), 升序 (大值向后排)
  for (let i = 0; i < numsMerge.length; i++) {
    for (let k = 0; k < numsMerge.length - 1 - i; k++) {
      if (numsMerge[k] > numsMerge[k + 1]) {
        let temp = numsMerge[k]
        numsMerge[k] = numsMerge[k + 1]
        numsMerge[k + 1] = temp
      }
    }
  }

  // 冒泡排序 : 反向(向前置换), 升序
  for (let i = numsMerge.length-1; i >=0; i--) {
    // 向前置换 第二层循环索引的起始值相反 并且索引值递减!!!
    for (let k = numsMerge.length-i; k >= 0; k--) {
      if (numsMerge[k] > numsMerge[k - 1]) {
        let temp = numsMerge[k]
        numsMerge[k] = numsMerge[k - 1]
        numsMerge[k - 1] = temp
      }
    }
  }
```