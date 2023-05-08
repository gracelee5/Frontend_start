# 기본 문법과 주석
> 선택자 { 속성: 값; }

ex)
```CSS
div{
font-size: 50px;
color: blue;
text-decoration: underline;
```
->HTML에서 div 찾는 문법

* 한 선택자 안에 여러 속성을 넣을 수 있다.
* 속성과 값을 제대로 구분하기 위해 :과 ;을 쓴다

주석 처리 기호는 /* */ 이다

# 선언 방식
1. 내장 방식
HTML의 style 태그를 이용해 CSS를 작성하는 방식

2. 링크 방식
CSS 파일을 HTML의 link 태그로 연결하는 방법
```HTML
<link rel="stylesheet: href="./css/main.css">
```

3. 인라인 방식
HTML의 전역 속성으로 스타일 직접 추가
```HTML
div style="color: red; margin: 20px;"></div>
```

4. import 방식

CSS 내에서 다른 CSS 파일을 가져와 연결

HTML
```HTML
<link rel="stylesheet: href="./css/main.css">
```
main.css
```CSS
@import url("./box.css");
```

#선택자
1. 기본 선택자

* 전체 선택자   
'*' 기호로 표시하며 HTML의 모든 요소의 선택 가능

```CSS
* {
  color: red;
  }
  ```

* 태그 선택자      
태그의 이름으로 요소 선택   
기본 선택자의 * 들어가는 곳에 태그 이름 작성

* 클래스 선택자    
HTML에 있는 class 속성의 값으로 요소 선택   
맨 앞에 . 기호 사용
```CSS
.orange {
  color: red;
  }
  ```
  
* ID 선택자         
HTML의 id 속성의 값으로 요소 선택


2. 복합 선택자

* 일차 선택자   
기본 선택자를 두 개 이상 붙여 작성하며, 사용된 기본 선택자들을 동시에 만족시키는 요소 선택
```CSS
span.orange {
  color: red;
  }
  ```
태그가 span이면서 class="orange" 속성과 값을 모두 만족하는 요소 선택한 것임

* 자식 선택자   
기본 선택자 사이에 > 기호가 들어감   
선택을 위한 조건
```CSS
ul>.orange{
color: red;
}
```

* 하위 선택자   
* 기본 선택자 사이에 띄어쓰기 작성
```CSS
div .orange{
color: red;
}
```
div의 하위 
