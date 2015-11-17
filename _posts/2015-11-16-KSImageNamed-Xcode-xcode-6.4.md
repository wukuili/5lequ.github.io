---
layout: post
title: KSImageNamed-Xcode插件在xcode 6.4/6.3或其他版本中不能使用
description: "KSImageNamed-Xcode插件在xcode 6.4/6.3或其他版本中不能使用"
tags: [xcode插件]
image:
  background: 
comments: true
share: true
---

现在这个插件最新版貌似只支持xcode7 ,需要修改KSImageNamed-xcode中的一个配置文件，添加uuid才能使他支持xcode6.3或6.4
进入下载的插件项目包，按下面路径找到KSImageNamed-Info.plist文件
 /KSImageNamed-Xcode-master/KSImageNamed/KSImageNamed-Info.plist

