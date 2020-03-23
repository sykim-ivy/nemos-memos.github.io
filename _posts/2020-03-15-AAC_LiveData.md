---
layout: post
title: "[AAC] LiveData"
category: Android
tags: [Android]
---
-------------------
<br/>
Android MVVM 적용을 위해 공부중
<br/>
<br/>
# LiveData
-------------------
 : '<span class="color_pointEmeraldGreen">View</span>'와 '(그 View에 올릴) Data'를 연결하는 일종의 Bridge (<<중간객체역할)  
 - Observer 패턴을 따름 <br/>
   ->> **즉, 데이터의 변경이 일어났을때 콜백으로 받아 처리하는데 LifeCycle을 인지해 필요하지 않을땐 콜백이 실행되지 않음**
       예를들어 Activity에 선언되어있는 LiveData의 경우 Activity가 Start, Resume 상태일때는 콜백을 실행하지만 다른 액티비티로 넘어가있는 OnStop 등의 상태일때는 실행되지 않습니다.
 - ACC ViewModel에서 사용할경우 ViewModel을 만든 UI Controller(Acitivty나 Fragment)의 LiveCycle과 동일하게 작동
<br/>
<br/>
<br/>
## ViewModel의 라이프사이클
<br/>
<br/>
<br/>
## 등장배경
<br/>
<br/>
<br/>
## 사용법
<br/>
<br/>
<br/>
## 주의점
<br/>
<br/>
<br/>
  
## 커스텀 생성자 구현
<br/>
<br/>
<br/>
## Fragment끼리 데이터 공유 시
ViewModelProviders.of(getActivity()).get(SharedViewModel.class);
<br/>
<br/>
<br/>
-------------------
## 참조
**AAC LiveData**<br/>
* LiveData 개념&Acitivty라이프사이클에 따른 호출 : <https://medium.com/harrythegreat/jetpack-android-livedata-%EC%95%8C%EC%95%84%EB%B3%B4%EA%B8%B0-ed49a6f17de3>
* LiveData : <http://dktfrmaster.blogspot.com/2018/02/livedata.html>
