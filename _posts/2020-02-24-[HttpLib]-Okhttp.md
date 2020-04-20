---
layout: post
title: "[HttpLib] Okhttp : 효율적인 HTTP client 라이브러리"
category: Android
tags: [Android]
---

# Context
<div class="colorscripter-code" style="color:#f0f0f0;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important;overflow:auto"><table class="colorscripter-code-table" style="margin:0;padding:0;border:none;background-color:#272727;border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px;border-right:2px solid #4f4f4f"><div style="margin:0;padding:0;word-break:normal;text-align:right;color:#aaa;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div><div style="line-height:130%">4</div><div style="line-height:130%">5</div><div style="line-height:130%">6</div><div style="line-height:130%">7</div><div style="line-height:130%">8</div></div></td><td style="padding:6px 0;text-align:left"><div style="margin:0;padding:0;color:#f0f0f0;font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important;line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;<span style="color:#999999">/**</span></div><div style="padding:0 6px; white-space:pre; line-height:130%"><span style="color:#999999">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*&nbsp;필수&nbsp;객체&nbsp;생성&nbsp;등&nbsp;로직을&nbsp;위한&nbsp;초기화</span></div><div style="padding:0 6px; white-space:pre; line-height:130%"><span style="color:#999999">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*/</span></div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;<span style="color:#ff3399">private</span>&nbsp;fun&nbsp;initialize()&nbsp;{</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;binding&nbsp;<span style="color:#0086b3"></span><span style="color:#ff3399">=</span>&nbsp;DataBindingUtil.setContentView(<span style="color:#ff3399">this</span>,&nbsp;R.layout.activity_trip_main)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;viewModel&nbsp;<span style="color:#0086b3"></span><span style="color:#ff3399">=</span>&nbsp;ViewModelProviders.of(<span style="color:#ff3399">this</span>).get(TripListViewModel::<span style="color:#ff3399">class</span>.java)</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;}</div></div><div style="text-align:right;margin-top:-13px;margin-right:5px;font-size:9px;font-style:italic"><a href="http://colorscripter.com/info#e" target="_blank" style="color:#4f4f4ftext-decoration:none">Colored by Color Scripter</a></div></td><td style="vertical-align:bottom;padding:0 2px 4px 0"><a href="http://colorscripter.com/info#e" target="_blank" style="text-decoration:none;color:white"><span style="font-size:9px;word-break:normal;background-color:#4f4f4f;color:white;border-radius:10px;padding:1px">cs</span></a></td></tr></table></div>
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
* Okhttp 공식 사이트 : <https://square.github.io/okhttp/>
* Okhttp Github(최신 버전 확인) : <https://github.com/square/okhttp/>
* Okhttp 사용법 : <https://altongmon.tistory.com/726>

