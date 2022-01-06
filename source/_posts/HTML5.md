---
title: 常用HTML5
tags:
  - 前端
  - html
categories:
  - 前端
cover: https://w.wallhaven.cc/full/96/wallhaven-96ylld.jpg
---
# HTML5

### 新增语义化标签

以前布局，我们基本都是用div来做。div对于搜索引擎来说，是没有语义的、

- ```html
  <header></header> 		头部标签
  <nav></nav>				导航标签
  <article></article>		内容标签
  <section></section>		定义文档某个区域
  <aside></aside>			侧边栏标签
  <footer></footer>		尾部标签
  ```

- ![Snipaste_2021-05-27_13-23-25](D:\前端\笔记\前端照片\Snipaste_2021-05-27_13-23-25.png)

- 注意

  - 这些语义化标签主要是针对搜索引擎的
  - 这些新标签页面中可以使用多次
  - 在IE9,需要把这些元素转换为块级元素
  - 其实，我们移动端更喜欢使用这些标签
  - HTML5还增加了很多其他的标签，我们后面慢慢学

### 新增的多媒体标签

#### 视频：<video>

| 浏览器            | MP4                                                  | WebM | Ogg  |
| ----------------- | ---------------------------------------------------- | ---- | ---- |
| Intermet Explorer | YES                                                  | NO   | NO   |
| CHrome            | YES                                                  | YES  | YES  |
| Firefox           | YES从Firefox 21版本开始    Linux系统从Firefox 30开始 | YES  | YES  |
| Safari            | YES                                                  | NO   | NO   |
| Opera             | YES     从Opera 25版本开始                           | YES  | YES  |

语法：

```html
<video src="文件地址" controls="controls"></video>
```

兼容性处理

```html
<video width="320" height="240" controls>
	<source src="movie.mp4" type="video/mp4">
    <source src="movie.ogg" type="video/ogg">
    您的浏览器不支持video标签
</video> 
```

常见属性

| 属性     | 值                                          | 描述                                                        |
| -------- | ------------------------------------------- | ----------------------------------------------------------- |
| autoplay | autoplay                                    | 视频就绪自动播放(谷歌浏览器需要添加muted来解决自动播放问题) |
| controls | controls                                    | 向用户显示播放控件                                          |
| width    | pixels(像素)                                | 设置播放器宽度                                              |
| height   | pixels(像素)                                | 设置播放器高度                                              |
| loop     | loop                                        | 播放完是否继续播放该视频，循环播放                          |
| preload  | auto(预先加载视频) none(不应该预先加载视频) | 规定是否预加载视频(如果有了autoplay就忽略该属性)            |
| src      | url                                         | 视频url地址                                                 |
| poster   | Imgurl                                      | 加载等待的画面图片                                          |
| muted    | muted                                       | 静音播放                                                    |

#### 音频<audio>

当前<audio>元素支持三种音频格式

| 浏览器            | MP3  | Wav  | Ogg  |
| ----------------- | ---- | ---- | ---- |
| Intermet Explorer | YES  | NO   | NO   |
| Chrome            | YES  | YES  | YES  |
| Firefox           | YES  | YES  | YES  |
| Safari            | YES  | YES  | NO   |
| Opera             | YES  | YES  | YES  |

语法

```html
<audio src="" ></audio>
```

兼容性问题

```html
<audio controls>
	<source src="horse.ogg" type="audio/ogg">
    <source src="horse.mp3" type="audio/mpeg">
    您的浏览器不支持audio元素
</audio> 
```

常见属性

| 属性     | 值       | 描述                                           |
| -------- | -------- | ---------------------------------------------- |
| autoplay | autoplay | 如果出现该属性，则音频在就绪后马上播放         |
| controls | controls | 如果出现该属性，则向用户显示控件，比如播放按钮 |
| loop     | loop     | 如果出现该属性，则每当音频结束时重新开始播放   |
| src      | url      | 要播放的音频的URL                              |

#### 多媒体标签总结

- 音频标签和视频标签使用方法基本一致
- 浏览器支持情况不同
- 谷歌浏览器把视频和音频的自动播放禁止了
- 我们可以给视频标签添加muted属性来静音播放视频，音频不可以(可以通过JS来解决)
- 视频标签是重点，我们经常设置自动播放，不使用controls控件，循环和设置大小属性

### 新增的input类型

| 属性值        | 说明                        |
| ------------- | --------------------------- |
| type="email"  | 限制用户输入必须是Email类型 |
| type="url"    | 限制用户输入必须是URL类型   |
| type="data"   | 限制用户输入必须是日期类型  |
| type="time"   | 限制用户输入必须是时间类型  |
| type="month"  | 限制用户输入必须是月类型    |
| type="week"   | 限制用户输入必须是周类型    |
| type="number" | 限制用户输入必须是数字类型  |
| type="tel"    | 手机号码                    |
| type="search" | 搜索框                      |
| type="color"  | 生成一个颜色选择表单        |

| 属性         | 值        | 说明                                                         |
| ------------ | --------- | ------------------------------------------------------------ |
| required     | required  | 表单拥有该属性表示其内容不能为空                             |
| placeholder  | 提交文本  | 表单的提示信息，存在默认值将不在显示                         |
| autofocus    | autofocus | 自动聚焦属性，页面加载完成自动聚焦到指定表单                 |
| autocomplete | off/on    | 当用户在字段开始键时，浏览器基于之前键入过的值，应该显示出在字段中填写的选项                              默认已经打开了，如autocompete="on"，关闭autocomplete="off"需要放在表单内，同时加上name属性，同时成功提交 |
| multiple     | multiple  | 可以多选文件提交                                             |

```CSS
/*可以通过以下设置方式修改placeholder里面的字体颜色*/
input::placeholder{
    color:pink;
}
```

### classList 属性

classList属性是HTML5新增的一个属性，返回元素的类名。但是ie10以上版本支持。

 该属性用于在元素中添加，移除及切换 CSS 类。有以下方法

**添加类：**

element.classList.add('类名');

```javascript
focus.classList.add('current');
```

**移除类：**

element.classList.remmove('类名')；

```javascript
focus.classList.remove('current');
```

**切换类：**

element.classList.toggle('类名')；

```javascript
focus.classList.toggle('current');
```

注意以上方法里面，所有类名都不带点
