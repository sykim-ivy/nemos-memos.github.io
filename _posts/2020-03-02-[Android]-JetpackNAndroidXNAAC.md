---
layout: post
title: "[Android][개념잡기] Jetpack & AndroidX & AAC"
category: Android
tags: [Android]
---
-------------------
  
# Jetpack
-------------------
 : Jetpack은 개발자가 고품질 앱을 손쉽게 개발할 수 있게 돕는 라이브러리, 도구, 가이드 모음 
 - 일종의 <span class="color_pointEmeraldGreen_Bold">Guidance</span>이며, 권고하는 라이브러리들과 도구들 모음 (귀여운 로고 관심없지만 있음)  
 - [객관적번역] 개발자 경험 향상을 위한 큰 범위의 노력 <span class="color_blurredGray">@from Quote from Alan Viverette (from Android Framework Team)</span>  
 - 플랫폼 API와는 별도로 제공되는 <span class="color_pointEmeraldGreen_Bold">androidx.*</span> 패키지 라이브러리로 구성됩니다. 
   
 #### Jetpack Component
 - 공식사이트에도 있지만 왠지 [이 설명 및 그림](https://beomseok95.tistory.com/189)이 더 좋아
<br/>
  
# AndroidX
-------------------
 : Jetpack 내에서 라이브러리를 개발, 테스트, 패키징, 버전 관리, 릴리즈에 사용하는 오픈소스 프로젝트
 - 하나의 <span class="color_pointEmeraldGreen_Bold">라이브러리</span>이며, 기술적 보증 (귀여운 로고 관심없고 없음)  
 - [객관적번역] Jetpack의 기술적인 기반 형성한 것 <span class="color_blurredGray">@from Quote from Alan Viverette (from Android Framework Team)</span>  
 - com.android.support.* 라이브러리들을 하나로 통합한 것
 - androidx 네임스페이스 내의 아티팩트가 Android Jetpack 라이브러리를 구성함
 - 컴파일 SDK 버전이 9.0(API 28) 이상 + gradle.properties 파일에 플래그 true 설정 필요
   
<br/>
  
# AAC = Android Architecture Component
-------------------
 : 
 - Jetpack 프로젝트의 섹션 중 하나
<br/>
 
<br/>
<br/>
<br/>
   
-------------------
## 참조
* Jetpack 공식사이트 : <https://developer.android.com/jetpack?hl=ko>
* Jetpack Component : <https://beomseok95.tistory.com/189>
* Jetpack, AndroidX 구분 : <https://pluu.github.io/blog/android/io18/2018/05/14/io-android-jetpack-whats-new-in-android-support-library/>
* Jetpack, AndroidX 구분 : <https://stackoverflow.com/a/50251717>

* AndroidX 공식 : <https://developer.android.com/jetpack/androidx>
* AndroidX란 : <https://eunplay.tistory.com/62>
* AndroidX란 : <https://cishome.tistory.com/146>
* AndroidX란 : <https://record-king.tistory.com/9>
