---
layout: post
title: "[AndroidView] Adapter & AdapterView"
category: Android
tags: [Android]
---
-------------------
  
안드로이드에는 <span class="color_pointEmeraldGreen">동일한 뷰 구조</span>가 반복되는 경우가 있다. ex) ListView, GridView<br/>
<span class="color_pointEmeraldGreen">하나의 Object(객체)로서, 보여지는 View</span>가 반복된다는 비유가 더 맞는 것 같다.<br/>
이런 구조(?)들의 뷰와 데이터를 관리하는데 필요한 것이 Adapter와 AdapterView.<br/>
  
<span class="color_pointRed">※ RecyclerView의 등장으로 잘 사용하지는 않는다만 원리 파악하고 있으면 좋다</span>
  
  
# Adapter
-------------------
 : '<span class="color_pointEmeraldGreen">View</span>'와 '(그 View에 올릴) Data'를 연결하는 일종의 Bridge (<<중간객체역할)  
 - 데이터 받고 관리 <span class="color_blurredGray"> >> set Data</span>  
 - **AdapterView**가 출력할 수 있는 형태로 데이터를 제공 (**※ 주의 : View를 화면에 출력 하지 않음!** )  <span class="color_blurredGray"> >> Data를 View 출력 형태로 가공</span>  

## Adapter Structure in Android
 - [여기](https://m.blog.naver.com/PostView.nhn?blogId=gi_balja&logNo=221162720020&proxyReferer=https%3A%2F%2Fwww.google.com%2F&view=img_2) 엄청 그림으로 잘 그려놓으셨습니다.
<br/>
<br/>
<br/>
  
# AdapterView
-------------------
 : <span class="color_pointEmeraldGreen">하나의 Object(객체)로서, 보여지는 View</span>들을 모두 보여주는 View  
AdapterView는 ViewGroup을 상속받으므로, 내부적으로 많은 뷰들을 담을 수 있다.  
ListView, GridView, Spinner 등이 AdapterView를 상속받고 있다  
 - **Adapter**가 출력할 수 있는 형태로 가공한 데이터를 받아 화면에 출력  
  
## AdapterView 동작원리 
  
 - [좋은 그림 및 설명 참조](https://okky.kr/article/396324)  

1) **Adapter객체 생성** 후 **AdapterView에 setAdapter()**  
2) **AdapterView**에서 **Adapter의 Observer객체를 등록** : AdapterView$AdapterDataSetObserver  
3) **AdapterDataObserver**에서 **아이템 숫자만큼 onChanged() 호출**  
4) onChanged() 단계에서 각 아이템 view들이 자기자신을 requestLayout() 호출  
5) **AdapterView는 자신의 자식이 붙어있는지를 확인**<span class="color_blurredGray">(안드로이드 View가 그려지는 라이프사이클에 따라 ononMeasure() -> 4번 전달받음 -> obtainView())</span> 후, **아이템의 수 만큼 getview() 호출**  
6) 이후 데이터에 변경이 있어 **notifydatasetChanged() 등의 함수 호출시 3번 진행**  
  
<span class="color_pointRed">※ 요약 :  **AdapterView**는 화면 드로잉에 필요한 정보를 **Adapter**에게 요청하게 되고,   **Adapter**는 자신이 가지고 있는 데이터를 가지고 요청받은 정보를 **AdapterView**에 리턴</span>  
  
  
## Adapter의 getView() 메소드
<div style="
    font-weight: 600;
    font-size: 19px;" class="border_light">
    abstract fun getView(int position, View convertView, ViewGroup parent): View
</div>
: 화면이 그려져야하는 시점에 호출되어 데이터들이 각 <span class="color_pointEmeraldGreen">View</span>들이 어떻게 보일지 뷰 그려서 반환  
  
#### getView() 파라미터 convertView는?
- #1) 기존에 화면에 그렸던 뷰가 존재하지 않으면, null값이 전달됨
- #2) 이전에 화면에 그려졌다가 보이지 않게 된 뷰가 존재한다면, null이 아닌 값이 전달됨    
  * 4.0 이후에는 화면에서 사라지는 순서대로 넘어오는 듯하다.
  * 이 Recycling 기법으로, 어댑터뷰는 화면에 표시할 최소한의 뷰만을 생성하게 된다.
  
#### getView() 최적화 #1 : View Holder 패턴
- 뷰 전개(inflating)은 매우 비싼 연산이므로 convertView안에 <span class="color_pointEmeraldGreen">View</span>에 맞춰 만든 Viewholder 클래스를 태그로 저장 및 재활용하는 방법  
- convertView가 null이면 Holder 객체를 생성하고 생성한 Holder 객체에 inflating 한 뷰의 참조값을 저장  
- convertView가 null이 아니면 뷰를 생성할때 태그에 저장했던 Holder 객체가 존재하므로 이를 가져와 속성값 등만 변경 이 Holder 객체는 자신을 inflating한 참조값 <span class="color_blurredGray">(다시 전개할 필요가 없다.)
{% highlight java linenos %}
// 전개된 뷰의 참조값을 저장할 객체
private class ViewHolder {
    private TextView textName;
    private ImageView imgName;
}

// 어댑터의 getView 메서드
@Override
public View getView(int position, View convertView, ViewGroup parent) {
    ViewHolder holder;

 if(convertView == null) {
     // convertView가 null이면 Holder 객체를 생성하고 
     // 생성한 Holder 객체에 inflating 한 뷰의 참조값을 저장
        holder = new ViewHolder();

        convertView = inflater.inflate(R.layout.layout_list_item, parent, false);
        holder.textName = (TextView) convertView.findViewById(R.id.text_item_name);
        holder.imgName = (ImageView) convertView.findViewById(R.id.img_item_name);
        
        // View의 태그에 Holder 객체를 저장
        convertView.setTag(holder);
    } else {
     // convertView가 null이 아니면 뷰를 생성할때 태그에 저장했던 Holder 객체가 존재
        // 이 Holder 객체는 자신을 inflating한 참조값(다시 전개할 필요가 없다.)
        holder = (ViewHolder) convertView.getTag();
    }

 // 속성값 변경
    ParcelableModel parcelableModel = getItem(position);
    holder.textName.setText(parcelableModel.name);
    if(parcelableModel.gender.equals('F')) {
        holder.imgName.setImageResource(R.drawable.female);
    } else if(parcelableModel.gender.equals('M')){
        holder.imgName.setImageResource(R.drawable.male);
    } else {
      holder.imgName.setImageResource(R.drawable.gender_default);
    }
    
    return convertView;
}
{% endhighlight %}

#### getView() 최적화 #2 : 지연 로딩(Lazy Loading)
- 항목중에 네트워크로부터 받아와야 하는 파일이 있을 경우,   getView에서 진행하게 되면 getView가 리턴되지 않아서 어댑터뷰의 화면이 그려지지 않아 화면이 멈추므로   비동기(ex) AsyncTask 등)으로 처리 -> 비동기 처리시 뷰를 바인딩하여, 작업이 완료된 후 자동적으로 뷰의 속성을 변경되도록 구현한다.  
- [여기](https://www.codehenge.net/2011/06/android-development-tutorial-asynchronous-lazy-loading-and-caching-of-listview-images/) 좋은 예제 참고
<br/>
<br/>
<br/>
  
-------------------
## 참조
* 개념 파악 & 예제 : <https://www.crocus.co.kr/1581>
* 상위 구조 파악 : <https://m.blog.naver.com/PostView.nhn?blogId=gi_balja&logNo=221162720020&proxyReferer=https%3A%2F%2Fwww.google.com%2F>
* AdapterView의 동작원리 : <https://okky.kr/article/396324>
* 작동원리 : <http://dktfrmaster.blogspot.com/2016/09/adapter-view.html>
* Lazy Loading 예제 : <https://www.codehenge.net/2011/06/android-development-tutorial-asynchronous-lazy-loading-and-caching-of-listview-images/>
