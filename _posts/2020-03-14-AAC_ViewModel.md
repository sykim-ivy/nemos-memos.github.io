---
layout: post
title: "[AAC] ViewModel"
category: Android
tags: [Android]
---
-------------------
<br/>
Android MVVM 적용을 위해 공부중
<br/>
<br/>
# ViewModel
-------------------
 : '<span class="color_pointEmeraldGreen">View</span>'와 '(그 View에 올릴) Data'를 연결하는 일종의 Bridge (<<중간객체역할)  
 - 데이터 받고 관리 <span class="color_blurredGray"> >> set Data</span>  
 - **AdapterView**가 출력할 수 있는 형태로 데이터를 제공 (**※ 주의 : View를 화면에 출력 하지 않음!** )  <span class="color_blurredGray"> >> Data를 View 출력 형태로 가공</span>  
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
**AAC ViewModel**<br/>
* ViewModel 등장배경&사용법&라이프사이클&Fragment 간 데이터 공유 : <https://woovictory.github.io/2019/05/02/What-is-ViewModel/>
* 위 블로그의 다수 참조 원본 : <https://duzi077.tistory.com/196>
* ViewModel 개념&사용법&주의점&커스텀 생성자 : <https://medium.com/@jungil.han/%EC%95%84%ED%82%A4%ED%85%8D%EC%B2%98-%EC%BB%B4%ED%8F%AC%EB%84%8C%ED%8A%B8-viewmodel-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-2e4d136d28d2>
* LiveData에서 같은 ViewModel 재사용이 가능한가? : <https://stackoverflow.com/questions/49364550/android-livedata-how-to-reuse-the-same-viewmodel-on-different-activities/49365126#49365126>
* Helper Class란? : <https://overface.tistory.com/436>
