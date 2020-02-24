---
layout: post
title: "[Android] Context"
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
* Context 개념 : <http://blog.naver.com/huewu/110085457720>
* Context 쉽게 개념 파악  : <https://zxcv5500.tistory.com/258>
* Context종류 & Components별 Context 접근 : <http://sunphiz.me/wp/archives/tag/applicationcontext>
* Context 클래스 & Context종류 & Components별 Context 접근 : <https://www.charlezz.com/?p=1080>
* Context & ContextWrapper & ContextImpl & Context 종류 및 좋은 예제 : <https://black-jin0427.tistory.com/220>
* [StackOverflow] Difference between getContext() , getApplicationContext() , getBaseContext() and “this” : <https://stackoverflow.com/questions/10641144/difference-between-getcontext-getapplicationcontext-getbasecontext-and>
* [StackOverflow] getApplication(), getApplicationContext(), getBaseContext(), getContext(), Class.this : 
<https://stackoverflow.com/questions/10347184/difference-and-when-to-use-getapplication-getapplicationcontext-getbasecon> 
* [JUMP][잘 설명해놓았으나 아직 해석중] Context & 상속구조 : <https://wundermanthompsonmobile.com/2013/06/context/>
* [JUMP][아직 해석중] Context & 상속구조 : <http://ericyang505.github.io/android/Context.html>
* Context : <http://dev.youngkyu.kr/36>
