---
layout: post
title:  "Android Studio下使用百度地图"
date:   2017-04-26 20:43:59
author: Jia Chen
categories: Android_Studio
tags:	AS BaiduMap
cover:  "/assets/baidu_map.jpg"
---

去年参加超图比赛时做了安卓端的地图应用，到现在已经大半年了。这段时间刚好又要做安卓端的地图开发，就随着进度梳理一下简单的安卓端开发。我是在macOS上用Android Studio写的，和Windows差别不大（不得不表扬一下Android Studio，能在不同平台间完美切换）。

## 使用百度地图

选择百度地图是因为使用的人比较多，且相关的教程资料较多，比较容易有上手，但其实不同地图API的使用差别不大，可以根据需求选择，这里以百度地图为例。

### 申请密钥

利用百度地图进行开发时需要申请密钥，一个App对应一个密钥。[百度地图开放平台][BaiduAPI]中有详细的申请方法,这里不再赘述。

### 配置环境

新建一个CampusLife项目，包名为com.example.jc.campuslife。名字可自行定义。因为我们的工程和校园生活有关，所以起了这个名字。在开始编码之前需要将百度地图Android SDK准备好，[在这里下载SDK][downloadAPI]。可根据所需功能来选择相应的开发包。
下载完成后进行解压，将jar文件复制到项目的app/libs目录下，然后在src/main目录下新建一个jniLibs目录,将解压缩后的so动态库放入这个目录中。
![文件目录]({{ site.url }}/assets/addsdk.jpg)

### Code Snippets

You can use [highlight.js][highlight] to add syntax highlight code snippets:

Use the [Liquid][liquid] `{% raw %}{% highlight <language> %}{% endraw %}` tag to add syntax highlighting to code snippets.

For instance, this template...
{% highlight html %}
{% raw %}{% highlight javascript %}    
function demo(string, times) {    
  for (var i = 0; i < times; i++) {    
    console.log(string);    
  }    
}    
demo("hello, world!", 10);
{% endhighlight %}{% endraw %}
{% endhighlight %}

...will come out looking like this:

{% highlight javascript %}
function demo(string, times) {
  for (var i = 0; i < times; i++) {
    console.log(string);
  }
}
demo("hello, world!", 10);
{% endhighlight %}

Syntax highlighting is done using [highlight.js][highlight]. You can change the active theme in [head.html](https://github.com/bencentra/centrarium/blob/2dcd73d09e104c3798202b0e14c1db9fa6e77bc7/_includes/head.html#L15).

### Images

Lightbox has been enabled for images. To create the link that'll launch the lightbox, add <code>data-lightbox</code> and <code>data-title</code> attributes to an <code>&lt;a&gt;</code> tag around your <code>&lt;img&gt;</code> tag. The result is:

<a href="//bencentra.com/assets/images/falcon9_large.jpg" data-lightbox="falcon9-large" data-title="Check out the Falcon 9 from SpaceX">
  <img src="//bencentra.com/assets/images/falcon9_small.jpg" title="Check out the Falcon 9 from SpaceX">
</a>

For more information, check out the [Lightbox][lightbox] website.

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[BaiduAPI]:    http://lbsyun.baidu.com/index.php?title=androidsdk/guide/key
[downloadAPI]: http://lbsyun.baidu.com/sdk/download?selected=mapsdk_basicmap,mapsdk_searchfunction,mapsdk_lbscloudsearch,mapsdk_calculationtool,mapsdk_radar
[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
[highlight]:   https://highlightjs.org/
[lightbox]:    http://lokeshdhakar.com/projects/lightbox2/
[jekyll-archive]: https://github.com/jekyll/jekyll-archives
[liquid]: https://github.com/Shopify/liquid/wiki/Liquid-for-Designers
