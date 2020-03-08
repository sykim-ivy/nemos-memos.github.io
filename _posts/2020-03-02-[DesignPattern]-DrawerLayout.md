---
layout: post
title: "[AndroidView] DrawerLayout (androidx.drawerlayout.widget.DrawerLayout)"
category: Android
tags: [Android]
---
------------
  
  
  
# DrawerLayout
------------
- [DrawerLayout에 기초잡기 퍼펙트한 블로그](https://recipes4dev.tistory.com/139)
  
## DrawerLayout 주의사항
- 속성
- 에러 : DrawerLayout must be measured with MeasureSpec.EXACTLY error <https://stackoverflow.com/questions/31746072/drawerlayout-must-be-measured-with-measurespec-exactly-error>
  
  
<br/><br/><br/><br/>
# Navigaion Drawer 
#### Navigaion = DrawerLayout + NavigationView (+Toolbar)
------------
## NavigationView
 : Drawer로 펼쳐지는 영역의 View (예전에는 리스트뷰로 구현하였으나 더 편리하게 NavigationView가 등장)  
 - 아래 속성 구현 필요
 {% highlight xml linenos %}
 android:headerLayout="@layout/header_schedule_main"
 app:menu="@menu/menu_schedule_main"
 {% endhighlight %}

 - [예제](https://developer88.tistory.com/131)
  
<br/><br/><br/><br/>
# Toolbar
------------
- 앱바(AppBar)를 만들 때 사용
- 안드로이드 5.0 (API Level 21)부터 추가된 위젯(Widget) 
  cf) 액티비티 내부에 기본적으로 포함된 `ActionBar`는 레이아웃 XML에 액션바 위젯을 추가하지 않아도 테마가 앱바(App Bar)를 지원하면, ActionBar를 액티비티의 앱바(App Bar)로 사용할 수 있으나, 호환성이 낮음<br/>
- `Toolbar 사용시 필수과정`
  * Toolbar 위젯에 대한 Dependency 추가. (ex) implementation 'androidx.appcompat:appcompat:1.1.0')
  * 툴바를 사용할 레이아웃 XML에 Toolbar를 추가. (ex) <androidx.appcompat.widget.Toolbar ... )
  * 툴바를 사용할 액티비티에 ".NoActionBar"가 포함된 테마를 지정하여 기본 액션바가 사용되지 않게 만듦.
  * 툴바를 사용할 액티비티에 setSupportActionBar() 메서드를 호출하여 툴바를 액티비티의 앱바(App Bar)로 사용 명시해야함.

  
  
  
  

<br/><br/><br/><br/>
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
