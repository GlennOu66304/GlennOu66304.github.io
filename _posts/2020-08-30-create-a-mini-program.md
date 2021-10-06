---
layout: mypost
title: create a miniprogram
categories: [小程序]
---

## I.Run the first miniprogram project.

1.登陆自己的小程序账号：[微信公众账号](https://mp.weixin.qq.com/wxamp/home/guide?lang=zh_CN&token=462012686)  
2.安装开发者工具：[安装开发工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)  
3.Get the App ID from:[AppID](https://mp.weixin.qq.com/wxamp/devprofile/get_profile?token=1810895196&lang=zh_CN)  
App ID find:[App ID](https://developers.weixin.qq.com/miniprogram/dev/framework/quickstart/getstart.html#%E7%94%B3%E8%AF%B7%E5%B8%90%E5%8F%B7)  
4.Delet the all the project you have built and create a first project which you have.
[你的第一个小程序](https://developers.weixin.qq.com/miniprogram/dev/framework/quickstart/getstart.html#%E5%AE%89%E8%A3%85%E5%BC%80%E5%8F%91%E5%B7%A5%E5%85%B7)  
5.编译预览:[编译预览](https://developers.weixin.qq.com/miniprogram/dev/framework/quickstart/getstart.html#%E7%BC%96%E8%AF%91%E9%A2%84%E8%A7%88)  
6.Minipro grammer references:
[WXML](https://developers.weixin.qq.com/miniprogram/dev/framework/view/wxml/)  
[WXSS](https://developers.weixin.qq.com/miniprogram/dev/framework/view/wxss.html)  
[事件](https://developers.weixin.qq.com/miniprogram/dev/framework/view/wxml/event.html)
中文版文档：[开始](https://developers.weixin.qq.com/miniprogram/dev/framework/quickstart/getstart.html#%E7%94%B3%E8%AF%B7%E5%B8%90%E5%8F%B7)  
微信开放社区：[小程序](https://developers.weixin.qq.com/community/develop/question)  
[只要 5 分钟，让你立刻拥有自己的小程序 | 知晓云](https://www.ifanr.com/minapp/893319)  
[微信小程序开发教程--从零开始](https://www.jianshu.com/p/aaef5ceb3936)

## II.微信小程序基础：天气应用

### 1.Miniprogram enviroment build:

1.According to the video expaintion to modify the program model verision:[构建最简单 Hello World](https://classroom.udacity.com/courses/ud666-cn-1/lessons/dd213e99-451f-46e2-ad8c-026f373ce701/concepts/e85e1ef9-93fe-40e3-9b8a-7fbfcb674f92)  
2.Compilation the project and see the " hello world change in the editor"
3.Download the project from Github  
4.import the project into the miniprogram editor.  
5.download the Hobrew:[Homebrew install erro](https://github.com/GlennOu66304/CS-RESOURS-CENTER/blob/master/C%20language/Homebrew%20install%20erro.md)and [Git](https://git-scm.com/download/mac) to edit it.  
6.Link your download git with the old version of Git:

```
zt@ztdeMacBook-Air ~ % rm '/usr/local/bin/git'
zt@ztdeMacBook-Air ~ % brew link git
Linking /usr/local/Cellar/git/2.28.0...
Error: Could not symlink bin/git-cvsserver
Target /usr/local/bin/git-cvsserver
already exists. You may want to remove it:
  rm '/usr/local/bin/git-cvsserver'
To force the link and overwrite all conflicting files:
  brew link --overwrite git
To list all files that would be deleted:
  brew link --overwrite --dry-run git
zt@ztdeMacBook-Air ~ % brew link --overwrite git
Linking /usr/local/Cellar/git/2.28.0... 209 symlinks created
zt@ztdeMacBook-Air ~ % brew link git
Warning: Already linked: /usr/local/Cellar/git/2.28.0
To relink:
  brew unlink git && brew link git
```

7.Use git to check the branch code in the repository:

1.cd to the project path

```
zt@ztdeMacBook-Air ~ % cd /Users/zt/cn-wechat-weather
zt@ztdeMacBook-Air cn-wechat-weather % git checkout 2-5
error: Your local changes to the following files would be overwritten by checkout:
	app.json
Please commit your changes or stash them before you switch branches.
Aborting
zt@ztdeMacBook-Air cn-wechat-weather %
```

2. Git switch to the different branch:[切换代码到不同的分支](https://classroom.udacity.com/courses/ud666-cn-1/lessons/dd213e99-451f-46e2-ad8c-026f373ce701/concepts/87e8a98e-72c1-4f91-89a6-affcb43feaf5)

```
git checkout 1-1 -f
```

### 2.概览：搭建小程序页面

1.you need to understand the Rpx meaning, mobile screen Height = height / width X 750 rpx(all screen width is 750 rpx)
Aspect ratio(宽高比),you could see it in the simulator.

```
任何手机屏幕宽度都是 750 rpx，手机屏幕的高度则可以由宽高比计算得出。在模拟器中你可以看到 iPhone 7, iPhone 7 Plus 和 iPhone X 的宽高比。

iPhone 7 宽高比 375 x 667, 因此屏幕高度对应与 667 / 375 x 750 rpx = 1334 rpx
iPhone 7 Plus 宽高比 414 x 736，因此屏幕高度对应与 736 / 414 x 750 rpx = 1333.33 rpx
iPhone X 宽高比 375 x 812，因此屏幕高度对应与 812 / 375 x 750 rpx = 1624 rpx
```

[尺寸单位 rpx](https://classroom.udacity.com/courses/ud666-cn-1/lessons/78473538-c159-49b1-8b8d-6f4d661790ba/concepts/e16cff89-1a6b-4919-aab9-53bf3c95dd63)  
[rpx (responsive pixel)](https://developers.weixin.qq.com/miniprogram/en/dev/framework/view/wxss.html)

2.add 12° into the app and change the style:

1. add the text in the index index.wxml and change the style in the index.wxss file:
   [我的步骤](https://classroom.udacity.com/courses/ud666-cn-1/lessons/78473538-c159-49b1-8b8d-6f4d661790ba/concepts/8d4be8fb-9510-466e-a344-df12a5f84bdc)

行高是字号的 1.4 倍 2. Use the Git to check the code change:

```
git diff origin/1-1 origin/2-1
```

[查看，比较示范代码对应分支](https://classroom.udacity.com/courses/ud666-cn-1/lessons/78473538-c159-49b1-8b8d-6f4d661790ba/concepts/8d4be8fb-9510-466e-a344-df12a5f84bdc)

3.Add text description in the files:
1.create a new view in the index.wxml include your text content and class-id
2.create a new style in the index.wxss file,make sure that the line-height's size is
1.5 times than font-size.

4.Check the local files' change, you could use the:

```
git diff
```

check the repository's change, you could use the:

```
git checkout 2-2 -f

git diff origin/2-1 origin/2-2
```

[添加天气描述](https://classroom.udacity.com/courses/ud666-cn-1/lessons/78473538-c159-49b1-8b8d-6f4d661790ba/concepts/df599be0-b731-428d-be23-c81c7998a58b)

**5.add the background change in the file:[添加背景](https://classroom.udacity.com/courses/ud666-cn-1/lessons/78473538-c159-49b1-8b8d-6f4d661790ba/concepts/7380f130-273e-4de3-865f-a5506a9a9c2b)**

1.creat a wrapper to wrap the temp and the weather in the index.wxml file;  
2.fix the wrapper's height and color in the index.wxss file;

6.add a picture in the miniprogram:[添加天气描述图片](https://classroom.udacity.com/courses/ud666-cn-1/lessons/78473538-c159-49b1-8b8d-6f4d661790ba/concepts/958f399d-7b5d-42ea-96f1-f5104f080f97)  
1.add the image text in the index.wxml file;
2.fix the wrapper's height and color in the index.wxss file;

7.change the navigation bar color: you could change the color you want, file is in the app.json file.[页面配置](https://developers.weixin.qq.com/miniprogram/dev/framework/config.html#%E5%85%A8%E5%B1%80%E9%85%8D%E7%BD%AE)

```
"navigationBarBackgroundColor": "#ffffff"
```

[修改标题栏颜色](https://classroom.udacity.com/courses/ud666-cn-1/lessons/78473538-c159-49b1-8b8d-6f4d661790ba/concepts/496708ed-5073-461e-bfc5-b83e875b1a21)

### 3.使用网络数据

1.add the JS code in the index.js, you will see the"Hello world" in the console.log:
[真正的 Hello World!](https://classroom.udacity.com/courses/ud666-cn-1/lessons/f3f84830-e834-4dea-8195-79c1dacb2cd2/concepts/d87a7472-a2a1-48a2-9193-2ac07d287644)

```
Page({
  onLoad() {
    console.log("Hello World!")
  }
})
```

2.To use the Weather API, you need to add the follow the format below to use the API data.[天气 API 介绍](https://classroom.udacity.com/courses/ud666-cn-1/lessons/f3f84830-e834-4dea-8195-79c1dacb2cd2/concepts/34991191-5756-4bb9-b04f-b468d8a9fd13)  
1.API Link + /api/weather/now + ?city=XXX 市  
https://test-miniprogram.com/api/weather/now?city=上海市
https://test-miniprogram.com//api/weather/now?city=XXX市  
2.URL error fixing:[不是合法域名 的报错信息](https://classroom.udacity.com/courses/ud666-cn-1/lessons/f3f84830-e834-4dea-8195-79c1dacb2cd2/concepts/34991191-5756-4bb9-b04f-b468d8a9fd13)

3. Extract the JSON data:[获取 JSON 数据](https://classroom.udacity.com/courses/ud666-cn-1/lessons/f3f84830-e834-4dea-8195-79c1dacb2cd2/concepts/d47518d7-05a0-4692-aa7a-b8302f336b5d)

```
wx.request({
  url: 'https://test-miniprogram.com/api/weather/now',
  data: {
     city: '广州市'
  },
  success: res => {
    console.log(res)
  }
})
```

WeChat documeatation:[RequestTask wx.request(Object object)](https://developers.weixin.qq.com/miniprogram/dev/api/network/request/wx.request.html)

4.(提取气温和天气)[https://classroom.udacity.com/courses/ud666-cn-1/lessons/f3f84830-e834-4dea-8195-79c1dacb2cd2/concepts/dc363d58-0885-4567-888c-04ee8965ef54]

```
let result = res.data.result
let temp = result.now.temp
let weather = result.now.weather
console.log(temp, weather)
```

5.[展示动态变量](https://classroom.udacity.com/courses/ud666-cn-1/lessons/f3f84830-e834-4dea-8195-79c1dacb2cd2/concepts/cfe9564e-f769-4ca4-81a2-bb9238151f49)

```
//在 WXML 中
<view class="temp">{{nowTemp}}</view>
<view class="weather">{{nowWeather}}</view>

//在 Page 中
data: {
  nowTemp: '14°',
  nowWeather: '阴天'
}
```

Wechat documeatation:[内容绑定](https://developers.weixin.qq.com/miniprogram/dev/reference/wxml/data.html#%E5%86%85%E5%AE%B9)  
6.[更新气温和天气数据](https://classroom.udacity.com/courses/ud666-cn-1/lessons/f3f84830-e834-4dea-8195-79c1dacb2cd2/concepts/963f5f11-1505-4a49-b67a-324d69b2262c)

```
this.setData({
    nowTemp: temp,
    nowWeather: weather
})
```

[微信小程序 ES6——箭头函数中的 this 问题](https://my.oschina.net/u/4357035/blog/3313614)

7.[更新天气图片和导航栏颜色](https://classroom.udacity.com/courses/ud666-cn-1/lessons/f3f84830-e834-4dea-8195-79c1dacb2cd2/concepts/8f361330-8ba4-406e-9fd8-addb5c22873a)  
Image update:

```
// in Page
data{
    nowWeatherBackground: ""
}

// in success: res=>{...}
this.setData{
    nowWeatherBackground: '/images/' + weather + '-bg.png'
}

// in WXML
<image class="weather-bg" src="{{nowWeatherBackground}}" mode="scaleToFill"></image>
```

navagation bar update:

```
const weatherColorMap = {
 'sunny': '#cbeefd',
 'cloudy': '#deeef6',
 'overcast': '#c6ced2',
 'lightrain': '#bdd5e1',
 'heavyrain': '#c5ccd0',
 'snow': '#aae1fc'
}

wx.setNavigationBarColor({
       frontColor: '#000000',
       backgroundColor: weatherColorMap[weather],
})
```

[wx.setNavigationBarColor(Object object)](https://developers.weixin.qq.com/miniprogram/dev/api/ui/navigation-bar/wx.setNavigationBarColor.html)  
8.实现下拉刷新  
配置开启下拉刷新
app.json

```
"window":{
    "enablePullDownRefresh": true
}
```

我们可以在 Page 中添加 onPullDownRefresh() 函数，执行 console.log("refresh executed!") 语句确认函数被成功调用。为了将"点点点"显示出来，我还在配置 backgroundTextStyle 为 dark

下拉刷新时调用天气 API

```
wx.request({
   complete: ()=> {
       wx.stopPullDownRefresh()
   }
})
```

[wx.stopPullDownRequest](https://developers.weixin.qq.com/miniprogram/dev/api/ui/pull-down-refresh/wx.stopPullDownRefresh.html)

### 4.构建列表

### 5.第二个页面

## Resource list:

Tutorial:  
Wechat documeantation:[Miniprogram](https://developers.weixin.qq.com/miniprogram/en/dev/framework/)  
Mini Program introduction:[WeChat Mini Programs](https://mp.weixin.qq.com/cgi-bin/wx)  
 Udacity:[项目 新闻小程序](https://github.com/udacity/wmpnd-news)  
RUNOOB.com:[微信小程序开发资源汇总](https://www.runoob.com/w3cnote/wx-xcx-repo.html)  
[How and Why To Develop A WeChat Mini Program or Game](https://www.appinchina.co/services/wechat-miniprograms/)  
[What are WeChat Mini-Programs? A Simple Introduction](https://walkthechat.com/wechat-mini-programs-simple-introduction/)  
Blog:[学习微信小程序开发环境布置](http://glennou.cn/2017/09/09/%E5%BE%AE%E4%BF%A1%E5%B0%8F%E7%A8%8B%E5%BA%8F%E5%BC%80%E5%8F%91%E7%8E%AF%E5%A2%83%E5%B8%83%E7%BD%AE/)  
[How to Build a Reactive Multilingual Mini Program](https://medium.com/china-software-development/how-to-build-a-multilingual-mini-program-94319f4a2a6c)  
[Hello World! Build your first WeChat Mini-Program from Scratch](https://www.wechatmpguru.com/build-your-first-mini-program/)  
[WeChat Mini-programs Wiki](https://github.com/schmunk42/wechat-miniprogram-wiki)  
[Everything you need to know about WeChat Mini-Program component](https://medium.com/china-software-development/everything-you-need-to-know-about-wechat-mini-program-component-53d5b0a1df71)  
Other Resources

Video:  
Udacity:[微信小程序开发](https://cn.udacity.com/course/wechat-mini-program-nanodegree--nd666-cn)  
Udacity:[微信小程序基础：商城应用](https://cn.udacity.com/course/wechat-mini-program--ud666-cn-2)  
Udacity:[微信小程序基础：天气应用](https://cn.udacity.com/course/wechat-mini-program--ud666-cn-1)
