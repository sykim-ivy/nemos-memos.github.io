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
   
 #### Jetpack Components
 - **Architecture** : 구글에서 제안하는 안드로이드 아키텍처를 구현할 수 있는 기능들로 구성되어 있다. View를 포함한 UI 요소의 lifecycle management를 비롯하여 LiveData와 ViewModel, Room등의 기능이 여기에 포함
 - **Foundation** : 안드로이드 시스템의 핵심 기능을 담당하는 컴포넌트로, AppCompat을 비롯하여 코틀린 익스텐션과 Multidex 등이 포함
 - **Behavior** : 앱의 동작과 관련한 것들로 알림(notification)을 비롯하여 다운로드 매니저나 권한(permission) 관리 기능 등
 - **UI** : UI 개발과 사용의 일관성을 보장해주는 컴포넌트들이 여기에 해당되는데, Animation, Fragment, Layout등의 일관된 처리가 가능
   
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
 : Jetpack Component들 중에서 'Architecture'에 속하는 애들
 - Jetpack 프로젝트의 섹션 중 하나
   
 ## AAC 종류
* **Data Binding** : Declaratively bind observable data to UI elements
* **Lifecycles** : Manage your activity and fragment lifecycles
* **LiveData** : Notify views when underlying database changes
* **Navigation** : Handle everything needed for in-app navigation
* **Paging** : Gradually load information on demand from your data source
* **Room** : Fluent SQLite database access
* **ViewModel** : Manage UI-related data in a lifecycle-conscious way
* **WorkManager** : Manage your Android background jobs
<br/>
   
<br/>
<br/>
<br/>
   
-------------------
## 참조
* Jetpack 공식사이트 : <https://developer.android.com/jetpack?hl=ko>
* Jetpack Components : <https://beomseok95.tistory.com/189>
* Jetpack, AndroidX 구분 : <https://pluu.github.io/blog/android/io18/2018/05/14/io-android-jetpack-whats-new-in-android-support-library/> [좋은 번역 같은데 나중에 더 읽어봐야함 JUMP] 
* Jetpack, AndroidX 구분 : <https://stackoverflow.com/a/50251717>

* AndroidX 공식 : <https://developer.android.com/jetpack/androidx>
* AndroidX란 : <https://eunplay.tistory.com/62>
* AndroidX란 : <https://cishome.tistory.com/146>
* AndroidX란 : <https://record-king.tistory.com/9>

* AAC 공식 소개 : <https://developer.android.com/topic/libraries/architecture?hl=ko>
* AAC 요소 : <https://blog.naver.com/PostView.nhn?blogId=mym0404&logNo=221635008951>
