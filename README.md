# 期末项目APP设计

# [20 * 20投影片下载查看链接](https://github.com/xiaohangwangxin/API-Final-work/blob/master/20X20.ppsx)

|发布日期|2019\12|
|-|------|
|APP名称|搜搜|
|设计者|肖航|
|开发者|肖航|
|测试者|肖航|
|文件状态|完成|


# 价值主张设计
## 产品背景
当下旅游的人越来越多，到外地旅游的时候，都会不可避免的遇到不同地方的不同的特色美食，这个时候人们就会想去了解这些美食名字，美食的历史，美食的故事。但是在外出行，总有不方便询问的时候，或者是遇到交流障碍的问题，就无法获得想要的美食信息。如果这个时候可以有一个软件，可以快速帮助用户获取想要的美食信息，就可以很好的解决这一困扰

## 核心价值 （阐述）
帮助用户在外出的旅游或工作时，更**快捷**以及**便捷**地搜寻到想要了解的食物信息

## 加值宣言
目前在市场上还没有专门做食物信息搜索这类软件，我们通过接入各大开放平台的api来实现食物信息即时搜索功能

目前主要运用3种api功能；分别是**腾讯美食图片识别，百度菜品识别api，百度图像对比度增强api**

通过运用腾讯美食图片识别api，先检测图片是否为美食图片；

运用百度开放平台中的菜品识别api，根据拍摄照片，识别图片中菜品名称，获取菜品百科信息；

运用百度开放平台中图像质量检测api，发现是否存在模糊、失焦、噪点、锯齿、马赛克等情况，减少因为用户图像问题而带来的识别误差；



|优先级|痛点|
|-|------|
|优先级|运用腾讯美食图片识别api，先检测图片是否为美食图片|
|优先级|运用百度开放平台中的菜品识别api，根据拍摄照片，识别图片中菜品名称，获取菜品百科信息|
|次优先|运用百度开放平台中图像对比度增强api，发现是否存在模糊、失焦、噪点、锯齿、马赛克等情况，减少因为用户图像问题而带来的识别误差|


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
|美食图片识别|用户想要知道自己拍的照片是否为一种食物|次重要
|菜品识别|掏出了手机上传照片，希望返回想要知道的菜品信息|重要
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
**[产品链接]( http://nfunm083.gitee.io/api-final-app)**
## 原型下载链接
**[产品下载]( https://github.com/xiaohangwangxin/API-Final-work/blob/master/app%E5%8E%9F%E5%9E%8B.rp)**
## 产品功能介绍
###  1.**启动页介绍**

![启动页](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E5%90%AF%E5%8A%A8%E9%A1%B5.png)


此页为打开搜搜APP时的启动页，用户第一次使用软件时将出现下方的进入按钮，第二次使用app时将不会再出现，而是自动跳转进入软件

**跳转说明**

![启动页](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E5%90%AF%E5%8A%A8%E9%A1%B5%E8%B7%B3%E8%BD%AC.png)

### 2.**首页介绍**

![首页](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E9%A6%96%E9%A1%B5.png)

此页为进入app后出现的页面，在页面中可以打开相机功能进行图片拍摄搜索美食，也可以通过上传图片搜索美食。还可以通软件的搜索功能直接进行美食的信息搜索，页面下方的搜索历史是用户过往使用搜搜进行美食搜索的记录。右侧为用户的个人信息以及设置页面跳转按钮

**跳转说明**

![首页](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E9%A6%96%E9%A1%B5%E8%B7%B3%E8%BD%AC.png)

### 3.**拍照页面**

![拍照](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E6%8B%8D%E7%85%A7%E9%A1%B5%E9%9D%A2.png)

此页为进入拍照页面，用户点击拍摄按钮进行拍摄，也可通过相机镜头反转按钮切换相机镜头。
***软件在收到用户拍摄的照片后，将使用菜品识别api进行图像识别，为保障识别质量，还将运用图像对比度增强api增强图片效果。提高识别精度***

**跳转说明**

![拍照](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E6%8B%8D%E6%91%84%E8%B7%B3%E8%BD%AC.png)



### 4.**相册页面**

![相册页面](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E7%9B%B8%E5%86%8C%E9%A1%B5%E9%9D%A2.png)


此页为相册页面，用户可选中想要进行搜索的美食图片，然后点击下方的搜索按钮进行搜索。***软件在收到用户拍摄的照片后，将使用菜品识别api进行图像识别，为保障识别质量，还将运用图像对比度增强api增强图片效果。提高识别精度***

**跳转说明**

![相册页面](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E7%9B%B8%E5%86%8C%E8%B7%B3%E8%BD%AC.png)

### 5.**返回信息页面**

![返回信息页面](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E8%BF%94%E5%9B%9E%E4%BF%A1%E6%81%AF%E9%A1%B5%E9%9D%A2.png)

此页为返回信息页面，时软件根据用户拍摄照片或者上传照片后，运用菜品识别api进行图像识别，以及图像对比度增强api进行图像识别后返回的信息返回页面。此页面会将美食的基本信息展现出来，若用户想来了解更多，可点击了解更多链接，进行更多信息的查看

### 6.**返回的失败信息页面**

![返回的失败信息页面](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E8%BF%94%E5%9B%9E%E4%BF%A1%E6%81%AF%E9%A1%B5%E9%9D%A2%EF%BC%88%E5%A4%B1%E8%B4%A5%EF%BC%89.png)

此页为用户在拍摄照片或者上传照片后，进入到信息返回页面。若软件无法识别出用户上传图片中的美食信息，将会弹出以上页面，用户可点击重新搜搜按钮再次搜索

### 7.**历史信息页面**

![历史信息页面](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E5%8E%86%E5%8F%B2%E4%BF%A1%E6%81%AF%E9%A1%B5%E9%9D%A2.png)

此页为历史信息搜索页面是用户的过往搜索信息的保留页面，用户进入页面可再次查看美食信息

**跳转说明**

![历史信息页面](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E5%8E%86%E5%8F%B2%E4%BF%A1%E6%81%AF%E8%B7%B3%E8%BD%AC.png)

# 产品机器学习之API的输出入展示

## 一.API使用水平

* 菜品识别API：对菜品信息进行识别

  **[查看代码详情](https://github.com/xiaohangwangxin/API-Final-work/blob/master/Untitled.ipynb)**

**识别结果代码**

![成功识别](https://github.com/xiaohangwangxin/API-Final-work/blob/master/%E8%8F%9C%E5%93%81%E8%AF%86%E5%88%AB.png)


* 图像对比度增强API：增强图片效果  

**[查看代码详情](https://github.com/xiaohangwangxin/API-Final-work/blob/master/Untitled1.ipynb)**

**增强效果展示**

![识别效果](https://github.com/xiaohangwangxin/API-Final-work/blob/master/c.png)

* 美食图片识别API：检测图片是否为美食

![识别效果](https://github.com/xiaohangwangxin/API-Final-work/blob/master/41fefd21b38024fadd32cfc4c45f731.png)
   


**识别效果展示**






|API|输入|输出|
|-|-|-|
|菜品识别|菜品照片|菜品相关信息
|美食图片识别|菜品照片|确认是否为食物图片|
|图像对比度增强|菜品照片|效果更佳的菜品照|


## 二.API使用比较分析
### 菜品识别比较

|对比项|百度|腾讯|
|-|-|-|
|实现效果|可返回菜品信息|只能辨认是否为食物|
|成熟度|较高|较低|
|价格比较|分免费版，付费版，定制版|可免费试用|
|需求程度|可基本满足搜索需要|无法满足搜索美食信息需要|



### 图像对比度增强比较
|对比项|百度|腾讯|
|-|-|-|
|实现效果|可进行图像清晰度的增强|未有相关功能|
|成熟度|较高|无|
|价格比较|[不同细化功能有不同的计价方式，此为跳转链接](https://ai.baidu.com/ai-doc/IMAGEPROCESS/Fk3bclmxa)|无|
|需求程度|高|无|


#### 总结
比较了百度和腾讯两家提供的api端口，关于菜品识别方面，百度的识别功能已经进展到可以识别菜品的程度，然而腾讯的仍停留在识别图片中内容
是否为食物的程度；而关于图像的对比度增强以帮助菜品识别更好的确定识别对象的方面，腾讯还没有提供同类型的api接口。因此我们选用的api都是来自
百度提供的接口。

## 三..API使用后风险报告


### 1.关于百度菜品识别API：

限制：
* 图片大小不超过4M
* 最短边至少15px，最长边最大4096px
* 图片需要base64编码、去掉编码头后再进行urlencode*

百度的菜品识别API还在不断迭代，目前的*识别误差偏大*，很难识别出流质的食物，如咖喱，汤等，以及特征较为模糊的食物。并且*菜品库中的数据较少*，一些比较少见的菜无法进行识别，仍需不断扩充数据库。价格在目前的市场中因为无同类相似竞品，无法进行比较，也一定程度上的垄断了这一美食识别搜索的细分领域。


**使用价格**

每日500次免费调用额度，免费额度用尽后开始计费，价格如下：

月调用量（万次）|	菜品识别（元/千次）
|-|-|
0<月调用量<=5|0.70
5<月调用量<=10|	0.60
10<月调用量<=20	|0.50
20<月调用量<=50	|0.40
50<月调用量<=100|	0.35
100<月调用量|	0.30
> 说明： 调用失败不计费


### 2.关于图片对比度增强API：

限制：

* ase64编码后大小不超过4M
* 最短边至少64px，最长边最大4096px，长宽比3：1以内
* 提示：图片的base64编码是不包含图片头的，如（data:image/jpg;base64,）

图片的对比度增强效果还是需要进一步优化，目前的优化效果化石更趋于对图片亮度的提高，其他的一些对比度增强还是没有十分显著

**使用价格**

每个账户一次性共3000次免费调用额度，免费额度用尽后开始计费，价格如下：

月调用量（万次）|图像对比度增强（元/千次）
|-|-|
0<月调用量<=300|6
300<月调用量	|3.6

> 说明： 调用失败不计费


## 四.加分项


* 菜品识别API：[查看代码详情](https://github.com/xiaohangwangxin/API-Final-work/blob/master/Untitled.ipynb)

* 图像对比度增强API： [查看代码详情](https://github.com/xiaohangwangxin/API-Final-work/blob/master/Untitled1.ipynb)

* 美食图片识别API：[查看代码详情](https://github.com/xiaohangwangxin/API-Final-work/blob/master/Untitled1.ipynb)










































