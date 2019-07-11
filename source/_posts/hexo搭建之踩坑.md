---
title: hexo搭建之踩坑000
---
----

以上是文章摘要 <!--more--> 以下是余下全文 

### 1. git上新建repository(存储库)设置名称时注意!
<!-- 不使用插件的方法1:
{% asset_img repository_name.jpg repository_name %} -->
<!-- 不使用插件的方法2: -->
<img src="/images/repository_name.jpg">
### 2. 全局_config.yml配置注意！
  <img src="/images/hexo_05.png">
### 2. 发布带图片博客
##### 2-1. 不使用插件方法1:
  ① 站点配置 _config.yml
    ```
      post_asset_folder: true
    ```
  ② 图片存放规则:
  <img src="/images/hexo_01.png" title="图片存放路径">
  ③ 引入图片时路径写法:
  ```
  {% asset_img 图片名称.jpg 图片title说明 %}
  ```
  <!-- <img src="/img/hexo_02.png" title="引入图片写法"> -->


##### 2-2. 不使用插件方法2:
  ① 站点配置 _config.yml
    ```
      post_asset_folder: false
    ```
  ② 图片存放规则:
  <img src="/images/hexo_03.png" title="图片存放路径">
  ③ 引入图片时路径写法:
  ```html
  <!-- 路径写成: "/img/图片名称.png"  -->
  <img src="/images/图片名称.png" title="图片title说明">
  <!-- 或路径写成: "img/图片名称.png"   -->
  <img src="images/图片名称.png" title="图片title说明">
  ```
  <!-- <img src="/img/hexo_04.png" title="引入图片写法"> -->