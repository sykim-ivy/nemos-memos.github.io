---
layout: post
title: "[Android] Activity vs AppCompatActivity"
category: Android
tags: [Android]
---
-------------------
<br/>
포함관계는 아래와 같다. <br/>
**Activity ⊃ FragmentActivity ⊃ AppCompatActivity ⊃ ActionBarActivity**
 <br/>
 <br/>
 <br/>

# Activity
-------------------
 : 
<br/>
<br/>
<br/>
# AppCompatActivity는
-------------------
 : AppCompatActivity는 안드로이드 하위버전을 지원하는 액티비티
 - Support Library에 있는 클래스(<안드로이드 하위버전을 지원하기 위해 존재) 중 하나
 - 최신버전안드로이드만 지원하겠다 하시면 AppCompatActivity를 쓸필요는 없으나 새로운 API가 추가될때마다 매번 버전 확인하기는 번거로우니 SupportLibrary를 쓰신다면 AppCompatActivity를 쓰시는게 좋습니다.
 - Ex1) dispatchKeyShortcutEvent 이 메소드는 3.0미만의 단말기에서는 실행이 안되기때문에 AppCompatActivity를 사용
 - Ex2) 액션바역시 3.0이후에 나온 기능이라 3.0미만의 단말기에서는 동작할수 없기때문에 AppCompatActivity를 사용
<br/>
<br/>
<br/>
-------------------
## 참조
* 좋은 질문&답변 : <https://hashcode.co.kr/questions/1487/%EC%9D%BC%EB%B0%98-activity%EC%99%80-appcompatactivity%EC%9D%98-%EC%B0%A8%EC%9D%B4%EA%B0%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80%EC%9A%94>
* JUMP site : <https://themach.tistory.com/37>

