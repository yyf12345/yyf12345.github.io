---
title: 更新Blog时的一些注意点
date: 2022-01-06 14:42:25
tags:
categories:
  - 更新
cover: https://w.wallhaven.cc/full/4x/wallhaven-4xp5zv.jpg
---

## 1. 查看版本号

1. Hexo：
   在自己博客文档里面的package.json文档中搜索version即可找到
   
2. hexo-cli
   在package-lock.json文档中直接搜索hexo-cli
   
3. node

   node -v

4. git

   git version

## 2. markdown文档

1. markdown文档的格式要求

   https://www.runoob.com/markdown/md-tutorial.html

2. 表头 Front-matter

   ![](https://res.cloudinary.com/dqro6ugug/image/upload/v1641452691/blog/image-20220105151114207_ujaddi.png)

   1. page front-matter

      ![](https://res.cloudinary.com/dqro6ugug/image/upload/v1641452817/blog/image-20220105151235909_osjlbr.png)

   2. post front-matter

      ![](https://res.cloudinary.com/dqro6ugug/image/upload/v1641453046/blog/screenshot-butterfly.js.org-2022.01.05-15_13_00_damz5g.png)

3. 文章封面在front-matter中设置

   ```
   cover: '文章的url'
   ||
   cover: 
     # 是否显示文章封面
     index_enable: true
     aside_enable: true
     archives_enable: true
     # 封面显示的位置
     # 三个值可配置 left , right , both
     position: both
     # 当没有设置cover时，默认的封面显示
     default_cover: 
   ```

   

4. 外挂标签

   自行借鉴butterfly主题中的外挂标签使用：
   https://butterfly.js.org/posts/4aa8abbe/#Note-Bootstrap-Callout


## 3. 一些命令语句

1. 创建草稿

   ```
   hexo new draft "草稿标题"
   ```

   静态网站中不会出现草稿文章

2. 生成博客文章

   ```
   hexo new "文章标题"
   ```

3. 生程纯页面

   ```
   hexo new page "文章标题"
   ```

4. 生成静态文件

   ```
   hexo g
   ```

5. 渲染静态网站

   ```
   hexo s
   ```

## 4. 评论模块

emoji是借用其他人的emojiCDN，网址为：https://cungudafa.blog.csdn.net/article/details/105548858

自己建立valine.json或者valine.yml时一直没有调试出来，无法自行显示表情包，但我删除这些文件后，在_config.butterfly.yml中设置为如下代码，表情包便成功显示出来，并能够使用。
```
  emojiCDN: 'https://cdn.jsdelivr.net/gh/xaoxuu/cdn-assets/emoji/valine/'
  enableQQ: true # enable the Nickname box to automatically get QQ Nickname and QQ Avatar
  emojiMaps: {} 
```

## 5. 未解决的问题
1. 标签页和分类页的头部图片无法设置
