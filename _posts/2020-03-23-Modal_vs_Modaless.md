---
layout: post
title: "[Theory] Modal vs Modaless"
category: ProgrammingTheory
tags: [Theory]
---
-------------------
<br/>
Dialog를 띄울 때 결정해야하는 방식 
<br/>
# Modal
-------------------
 : 간단한 개념으로 Modal 창(=보통 dialog창)이 열렸을 때는 기존에 있던 화면(=창)을 사용하지 못하는 방식
<br/>
 - Modal창이 제어권을 독점하여 자신을 종료하기 전까지는 기존에 열린 모든 화면(=창=window) 작업 불가능. (응용 프로그램의 주 창의 작업 흐름을 방해)
 - 사용자의 명령을 인식하기 위해서나, 중요한 메세지, 긴급 상황을 알리기 위해 많이 사용
 - Ex) 우리가 자주 사용하는 파일 열기/저장 대화상자, visual studio의 정보 대화 상자나, api의 messagebox
<br/>
<br/>
# Modaless
-------------------
 : Modal과 반대 개념으로 Modaless 창(=보통 dialog창)이 열렸을 때도 기존에 있던 화면(=창)을 사용가능한 방식
<br/>
  - Modaless 사용자가 순서에 상관없이 어느 창이나 화면에든 접근이 가능 
  - 위로 인하여 프로그래밍 하기 더 어려움
  - 사용자에게 정보를 전달하는 경우 주로 사용
<br/>
<br/>
<br/>
<br/>
-------------------
## 참조
* Modal 위키 : <https://ko.wikipedia.org/wiki/%EB%AA%A8%EB%8B%AC_%EC%9C%88%EB%8F%84>
* 개념 : <https://lapislazull.tistory.com/80>
