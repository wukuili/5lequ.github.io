---
layout: post
title: tableView滑动时卡顿
description: "tableView滑动时卡顿"
tags: [ios,tableView]
image:
  background: witewall_3.png
comments: true
share: true
---
对于tableView滑动时卡顿的问题，主要原因是从缓存或是本地读取图片的时候需要耗费时间，解决方法是通过在子线程中加入如下代码即可
{% highlight object-c %}
NSData *imageData=[NSData dataWithContentsOfURL:[NSURL URLWithString:app.icon]];
UIImage *image=[UIImage imageWithData:imageData];
{% endhighlight %}
把UIImage赋值给图片的过程在主线程中进行，子线程不能更新UI，所有UI更新都在主线程，所以手指滑动屏幕的时候，就会在主线程中更新UI，就不会出现卡顿的现象

