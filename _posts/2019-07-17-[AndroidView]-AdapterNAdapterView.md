---
layout: post
title: "[AndroidView] Adapter & AdapterView"
category: Android
tags: [Android]
---
  
안드로이드에는 <span class="color_pointEmeraldGreen">동일한 뷰 구조</span>가 반복되는 경우가 있다. ex) ListView, GridView<br/>
<span class="color_pointEmeraldGreen">하나의 Object(객체)로서, 보여지는 View</span>가 반복된다는 비유가 더 맞는 것 같다.<br/>
이런 구조(?)들의 뷰와 데이터를 관리하는데 필요한 것이 Adapter와 AdapterView.<br/>
  
  
# Adapter
'<span class="color_pointEmeraldGreen">View</span>'와 '(그 View에 올릴) Data'를 연결하는 일종의 Bridge (<<중간객체역할)  
 - 데이터 받고 관리 <span class="color_blurredGray"> >> set Data</span>  
 - 어댑터뷰가 출력할 수 있는 형태로 데이터를 제공 <span class="color_blurredGray"> Data >> (가공) >> View</span>  
  
## Adapter Structure in Android
  [여기 엄청 그림으로 잘 그려놓으셨습니다.] (https://m.blog.naver.com/PostView.nhn?blogId=gi_balja&logNo=221162720020&proxyReferer=https%3A%2F%2Fwww.google.com%2F&view=img_2)

  
## AdapterView


To insert highlight code inside of a post, it's enough to use some specific tags, 
has directly described into the [Jekyll documentation](http://jekyllrb.com/docs/templates/#code-snippet-highlighting). 
In this way the code will be included into a ``.highlight`` CSS class and will be highlight according to the [syntax.scss]
(https://github.com/mojombo/tpw/blob/master/css/syntax.css) file. This is the standard style adopted by **Github** to highlight the code. 

This is a CSS example:
{% highlight css linenos %}

body {
  background-color: #fff;
  }

h1 {
  color: #ffaa33;
  font-size: 1.5em;
  }

{% endhighlight %}

And this is a HTML example, with a linenumber:
{% highlight html linenos %}

<html>
  <a href="example.com">Example</a>
</html>

{% endhighlight %}

Last, a Ruby example:
{% highlight ruby linenos %}

def hello
  puts "Hello World!"
end

{% endhighlight %}


## 참조
* 개념 파악 : <https://www.crocus.co.kr/1581>
* 상위 구조 파악 : <https://m.blog.naver.com/PostView.nhn?blogId=gi_balja&logNo=221162720020&proxyReferer=https%3A%2F%2Fwww.google.com%2F>
* 작동원리 : <http://dktfrmaster.blogspot.com/2016/09/adapter-view.html>
