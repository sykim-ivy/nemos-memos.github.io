---
layout: post
title: "[AndroidView] Adapter & AdapterView"
category: Android
tags: [Android]
---

# Context

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
