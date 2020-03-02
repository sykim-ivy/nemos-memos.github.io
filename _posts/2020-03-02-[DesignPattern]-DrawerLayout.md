---
layout: post
title: "[AndroidView] DrawerLayout (androidx.drawerlayout.widget.DrawerLayout)"
category: Android
tags: [Android]
---
------------
  

# DrawerLayout
------------
[좋은 뷰 개념까지 설명](https://recipes4dev.tistory.com/139)

## DrawerLayout 주의사항
- 속성
- 에러 : DrawerLayout must be measured with MeasureSpec.EXACTLY error <https://stackoverflow.com/questions/31746072/drawerlayout-must-be-measured-with-measurespec-exactly-error>
  
  
  
# Navigaion Drawer = DrawerLayout + NavigationView (+Toolbar)
------------
## NavigationView
 : Drawer로 펼쳐지는 영역의 View (예전에는 리스트뷰로 구현하였으나 더 편리하게 NavigationView가 등장)  
 - 아래 속성 구현 필요
 {% highlight xml linenos %}
 android:headerLayout="@layout/header_schedule_main"
 app:menu="@menu/menu_schedule_main"
 {% endhighlight %}

 - [예제](https://developer88.tistory.com/131)
  
  
# Toolbar
------------


  
  
  
  


## 참조
* DrawerLayout 개념 : <https://recipes4dev.tistory.com/139>
* DrawerLayout 예제 : <https://g-y-e-o-m.tistory.com/128>
* width,height값 잘 못 줄때 나는 에러 : <https://stackoverflow.com/questions/31746072/drawerlayout-must-be-measured-with-measurespec-exactly-error>

* Toolbar before Navigation Drawer : <https://developer88.tistory.com/50>
* Navigation Drawer : <https://developer88.tistory.com/131>
* 딱 원하는 예제 : <https://duzi077.tistory.com/167>

* Toolbar란 : <https://recipes4dev.tistory.com/149>
* Toolbar vs ActionBar / 등장배경 : <https://jw910911.tistory.com/63>
* Toobar 예제 : <https://lktprogrammer.tistory.com/167>
