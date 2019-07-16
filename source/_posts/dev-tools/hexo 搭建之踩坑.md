---
title: hexo 搭建之踩坑
entitle: 'hexo'
author: 小苏
authorDesc: 在写bug的康庄大道上一骑绝尘
avatar: /images/favicon.png
authorLink: 'https://www.???name.com'
authorAbout: 'https://about.???name.com'
categories: 开发工具
timestamp: 1528030114
date: 2018-09-06 17:10:35
tags:
    - hexo搭建
keywords: 
description: 搭建hexo时的各种坑
photos:
    # - /img/2018/15280267906540.jpg
---

## 一、hexo项目配置问题

### 1. git上新建repository(存储库)设置名称时注意!
![嵌入图片地址示例](/img/2019/repository_name.webp)

### 2. 全局_config.yml配置注意！
![嵌入图片地址示例](/img/2019/hexo_05.png)


## 二、文章发布问题

### 1. 文档基础参数
```js
title: 发文模版(文章名称)
entitle: '这个是当前文章上级目录名称, 注意!: 记得加引号'
author: 作者名称
avatar: /images/作者头像.png
authorLink: 'https://www.???name.com'
authorAbout: 'https://about.???name.com'
authorDesc: 在写bug的康庄大道上一骑绝尘
categories: 所属导航分类名称
timestamp: 1528030114  // 时间戳: 其具有唯一性, 是当前文档生成html后的文件名称!!!;
date: 2018-06-03 20:48:34  // 发布时间 可自定义
tags:
    - 具有标签属性1!
    - 具有标签属性2!
    - 具有标签属性3!
keywords: 当前技术seo关键词
description: 来自?时的笔记：对文章内容的简要概述
photos:
    # - /img/2018/15280267906540.jpg
```
### 2. 发布带图片博客
#### 2-1. 本主题下方法:
> md文档中写法:   `![嵌入图片](/img/2018/图片地址.jpg)`
![嵌入图片地址示例](/img/2019/imgLink.png)
##### 2-2. 网上分享说法1 (不借助插件 待测试):
  ① 站点配置 _config.yml
    ```
      post_asset_folder: true
    ```
  ② 图片存放规则:
    > `<img src="/images/hexo_01.png" title="图片存放路径">`
  ③ 引入图片时路径写法:
  ```
  {% asset_img 图片名称.jpg 图片title说明 %}
  ```


##### 2-3. 网上分享说法2 (不借助插件 待测试):
  ① 站点配置 _config.yml
    ```
      post_asset_folder: false
    ```
  ② 图片存放规则:
  > `<img src="/images/hexo_03.png" title="图片存放路径">`
  ③ 引入图片时路径写法:
  ```html
  <!-- 路径写成: "/img/图片名称.png"  -->
  <img src="/images/图片名称.png" title="图片title说明">
  <!-- 或路径写成: "img/图片名称.png"   -->
  <img src="images/图片名称.png" title="图片title说明">
  ```
  <!-- <img src="/img/hexo_04.png" title="引入图片写法"> -->