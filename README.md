# 期末项目APP设计

|发布日期|2019\12|
|-|------|
|APP名称|搜搜|
|设计者|肖航|
|开发者|肖航|
|测试者|肖航|
|文件状态|进行中|


# 价值主张设计
## 产品背景
当下旅游的人越来越多，到外地旅游的时候，都会不可避免的遇到不同地方的不同的特色美食，这个时候人们就会想去了解这些美食名字，美食的历史，美食的故事。但是在外出行，总有不方便询问的时候，或者是遇到交流障碍的问题，就无法获得想要的美食信息。如果这个时候可以有一个软件，可以快速帮助用户获取想要的美食信息，就可以很好的解决这一困扰

## 核心价值 （阐述）
帮助用户在外出的旅游或工作时，更**快捷**以及**便捷**地搜寻到想要了解的食物信息

## 加值宣言
目前在市场上还没有专门做食物信息搜索这类软件，我们通过接入各大开放平台的api来实现食物信息即时搜索功能

目前主要运用3种api功能；分别是**百度菜品识别api，百度图像效果增强api，图像质量检测api**

通过运用百度开放平台中的菜品识别api，根据拍摄照片，识别图片中菜品名称，获取菜品百科信息；

运用百度开放平台中图像效果增强api，解决图像偏小、不清晰、被拉伸、过暗或过亮等问题，减少因为用户图像问题而带来的识别误差；

运用百度开放平台中图像质量检测api，发现是否存在模糊、失焦、噪点、锯齿、马赛克等情况，减少因为用户图像问题而带来的识别误差；


|优先级|痛点|
|-|------|
|优先级|运用百度开放平台中的菜品识别api，根据拍摄照片，识别图片中菜品名称，获取菜品百科信息|
|次优先|运用百度开放平台中图像效果增强api，解决图像偏小、不清晰、被拉伸、过暗或过亮等问题，减少因为用户图像问题而带来的识别误差|
|次优先|运用百度开放平台中图像质量检测api，发现是否存在模糊、失焦、噪点、锯齿、马赛克等情况，减少因为用户图像问题而带来的识别误差|


##  目标用户
有需要进行美食搜索的客户群体

## 用户痛点 
- 在市场上还没有相似的专门做食物搜索的软件，用户需要这样一款软件
- 想了解美食信息的时候，因为交流障碍的问题，而无法获知美食的名称
- 用户在了解到菜品的名字后，可能会想了解到更多的关于菜品的制作方式，食材等更多信息
- 用户在拍照时，受制于客观环境条件因素，拍出来的图片表现效果不佳，照片出现模糊，过暗，过亮等情况，从而担心检测结果不准确

## 用户需求列表
|标题|用户使用情景|重要程度|
|-|-|-|
|菜品识别|掏出了手机上传照片，希望返回想要知道的菜品信息|重要
|图像质量检测|用户上传的图像可能会模糊不清的现象|次重要
|图像效果增强|用户上传的图像可能会过暗，偏小等情况|次重要|

## 用户画像
|人群|详情|
|-|-|
|群体|外出工作或者游玩的用户|
|年龄阶层|各年龄阶层|
|痛点|需要快速获知菜品信息，却因客观原因无法获知，存在获知的限制

## 人工智能概率性与用户痛点

在软件进行识别的过程中，会因为图像识别功能尚未完全完善的原因，不可避免地会出现测试误差的情况。就例如，咖喱饭，汤，等流质食物就暂时未能识别，在软件开发地过程中，我们会不断完善软件地数据库，增加菜品图库的容纳信息，不断降低识别的误差。在出现识别内容误差率超过 **80%** 的时候，软件将显示无法搜索出美食，不给用户提供错误新信息。

# 原型设计
## 原型产品链接
[产品链接]( http://nfunm083.gitee.io/api-final-app)
## 原型下载链接
[产品下载]( https://github.com/xiaohangwangxin/API-Final-work/blob/master/app%E5%8E%9F%E5%9E%8B.rp)
## 产品功能介绍
* 1.启动页介绍

![启动页](https://upload-images.jianshu.io/upload_images/9502831-9348fa67b6dd5d10.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


此页为打开搜搜APP时的启动页，用户第一次使用软件时将出现下方的进入按钮，第二次使用app时将不会再出现，而是自动跳转进入软件

* 2.首页介绍

![首页](https://upload-images.jianshu.io/upload_images/9502831-39ee84c0fab0bfe4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

此页为进入app后出现的页面，在页面中可以打开相机功能进行图片拍摄搜索美食，也可以通过上传图片搜索美食。还可以通软件的搜索功能直接进行美食的信息搜索，页面下方的搜索历史是用户过往使用搜搜进行美食搜索的记录。右侧为用户的个人信息以及设置页面跳转按钮

* 3.拍照页面

![拍照](https://upload-images.jianshu.io/upload_images/9502831-5749ab0a2f1c52fb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

此页为进入拍照页面，用户点击拍摄按钮进行拍摄，也可通过相机镜头反转按钮切换相机镜头。
***软件在收到用户拍摄的照片后，将使用菜品识别api进行图像识别，为保障识别质量，还将运用图像质量检测api，以及图像效果增强api增强图片效果。提高识别精度***

* 4.相册页面

![相册页面](https://upload-images.jianshu.io/upload_images/9502831-9be89544a9315d19.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


此页为相册页面，用户可选中想要进行搜索的美食图片，然后点击下方的搜索按钮进行搜索。***软件在收到用户拍摄的照片后，将使用菜品识别api进行图像识别，为保障识别质量，还将运用图像质量检测api，以及图像效果增强api增强图片效果。提高识别精度***

* 5.返回信息页面

![返回信息页面](https://upload-images.jianshu.io/upload_images/9502831-736ae5183e750265.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

此页为返回信息页面，时软件根据用户拍摄照片或者上传照片后，运用菜品识别api进行图像识别，图像质量检测api，以及图像效果增强api进行图像识别后返回的信息返回页面。此页面会将美食的基本信息展现出来，若用户想来了解更多，可点击了解更多链接，进行更多信息的查看

* 6.返回的失败信息页面

![返回的失败信息页面](https://upload-images.jianshu.io/upload_images/9502831-a4130b05de6aedc1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

此页为用户在拍摄照片或者上传照片后，进入到信息返回页面。若软件无法识别出用户上传图片中的美食信息，将会弹出以上页面，用户可点击重新搜搜按钮再次搜索

* 7.历史信息页面

![历史信息页面](https://upload-images.jianshu.io/upload_images/9502831-1db2e5fee35538bc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

此页为历史信息搜索页面是用户的过往搜索信息的保留页面，用户进入页面可再次查看美食信息

# API 产品使用关键AI或机器学习之API的输出入展示





































