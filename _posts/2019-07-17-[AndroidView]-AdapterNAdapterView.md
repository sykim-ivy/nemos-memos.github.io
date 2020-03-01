---
layout: post
title: "[AndroidView] Adapter & AdapterView"
category: Android
tags: [Android]
---
  
안드로이드에는 <span class="color_pointEmeraldGreen">동일한 뷰 구조</span>가 반복되는 경우가 있다. ex) ListView, GridView<br/>
<span class="color_pointEmeraldGreen">하나의 Object(객체)로서, 보여지는 View</span>가 반복된다는 비유가 더 맞는 것 같다.<br/>
이런 구조(?)들의 뷰와 데이터를 관리하는데 필요한 것이 Adapter와 AdapterView.<br/>
  
<span class="color_pointRed">RecyclerView의 등장으로 잘 사용하지는 않는다만 원리 파악하고 있으면 좋다</span>
  
  
# Adapter
'<span class="color_pointEmeraldGreen">View</span>'와 '(그 View에 올릴) Data'를 연결하는 일종의 Bridge (<<중간객체역할)  
 - 데이터 받고 관리 <span class="color_blurredGray"> >> set Data</span>  
 - **AdapterView**가 출력할 수 있는 형태로 데이터를 제공 <span class="color_blurredGray"> Data >> (View 출력 형태로 가공, **※ 주의 : View를 화면에 출력 하지 않음!**) </span>  
  
## Adapter Structure in Android
  [여기 엄청 그림으로 잘 그려놓으셨습니다.] (https://m.blog.naver.com/PostView.nhn?blogId=gi_balja&logNo=221162720020&proxyReferer=https%3A%2F%2Fwww.google.com%2F&view=img_2)

  
## AdapterView
<span class="color_pointEmeraldGreen">하나의 Object(객체)로서, 보여지는 View</span>들을 모두 보여주는 View  
ListView, GridView, Spinner 등이 AdapterView를 상속받고 있다  
 - **Adapter**가 출력할 수 있는 형태로 가공한 데이터를 받아 화면에 출력  
  
# AdapterView 동작원리 
[좋은 그림 및 설명 참조] : (https://okky.kr/article/396324)  
1) **Adapter**객체 생성 후 **AdapterView**에 **setAdapter()**
2) **AdapterView**에서 **Adapter**의 Observer객체를 등록 : **AdapterView$AdapterDataSetObserver**  
3)  **AdapterDataObserver**에서 객체 숫자만큼 onChanged() 호출
4) onChanged() 단계에서 각 view들이 자기자신을 requestLayout() 호출  
5) **AdapterView**는 자신의 자식이 붙어있는지를 확인<span class="color_blurredGray">(안드로이드 View가 그려지는 라이프사이클에 따라 ononMeasure() > 4번 전달받음 > obtainView())</span> 후, 아이템의 수 만큼 getview() 호출
+ 6) 이후 데이터에 변경이 있어 notifydatasetChanged() 등의 함수 호출시 3번 진행 


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
* 개념 파악 & 예제 : <https://www.crocus.co.kr/1581>
* 상위 구조 파악 : <https://m.blog.naver.com/PostView.nhn?blogId=gi_balja&logNo=221162720020&proxyReferer=https%3A%2F%2Fwww.google.com%2F>
* AdapterView의 동작원리 : <https://okky.kr/article/396324>
* 작동원리 : <http://dktfrmaster.blogspot.com/2016/09/adapter-view.html>
