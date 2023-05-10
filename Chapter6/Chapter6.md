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

* 일치 선택자   
기본 선택자를 두 개 이상 붙여 작성하며, 사용된 기본 선택자들을 동시에 만족시키는 요소 선택
```CSS
span.orange {
  color: red;
  }
  ```
태그가 span이면서 class="orange" 속성과 값을 모두 만족하는 요소 선택한 것임

* 자식 선택자   
기본 선택자 사이에 **>** 기호가 들어감   
선택을 위한 조건
ul의 자식 요소 중 class="orange" 속성과 값을 포함한 요소 선택
```CSS
ul>.orange{
color: red;
}
```

* 하위 선택자   
기본 선택자 사이에 **띄어쓰기** 작성
```CSS
div .orange{
color: red;
}
```
div의 하위 요소 중 class="orange" 속성과 값을 포함한 모든 요소 선택

* 인접 형제 선택자   
기본 선택자 사이에 **+** 기호 들어감
```CSS
.orange + li{
color: red;
}
```
li 태그 선택자로 요소 선택하는데 class="orange" 속성과 값을 포함한 요소의 인접한 다음 형제 요소

* 일반 형제 선택자   
기본 선택자 사이에 ~ 기호 들어감   
모든 다음 형제 요소들을 의미


3. 가상 클래스 선택자
가상 클래스 선택자는 : 기호로 시작됨 이 뒤에 뭐가 붙느냐에 따라 선택자의 역할이 조금씩 달라짐

**:hover**
어떤 요소에 마우스 커서가 올라간 상태   
요소에 마우스가 올라간 상태에서만 요소를 선택함
```CSS
a:hover{
  color: red;
  }
```
마우스 커서가 올라간 상태에서만 빨간색으로 출력

**:active**
요소를 마우스로 선택하고 있는 동안에만 요소 선택   
ex) 링크 클릭하는 동안에 색이 바뀜

**:focus**   
대화형 요소가 활성화 되면 요소 선택   
ex) 텍스트 박스 활성화 되면 색 바뀜

**:first-child, :last-child**
:first child는 첫번째 자식 요소 선택   
:last child는 마지막 자식 요소 선택

**:nth-child(n)**   
n번째 자식 요소 선택

**:not(s)**   
부정 선택자로 소괄호 사이에 부정할 선택자 s 표시

4. 가상 요소 선택자
:: 기호로 시작함   
HTML 구조에 CSS로 가상의 요소를 생성 또는 삽입할 수 있음   
CSS의 content 속성과 꼭 같이 사용해야 함 

**::before**
요소의 내부 앞에 가상의 요소를 삽입   
HTML
```HTML
<div class="box">
  Content!
</div>
```
CSS
```CSS
.box::before{
content: "앞!";
}
```
출력 : 앞! Content!

**::after**
요소의 내부 뒤에 가상의 요소 삽입   
HTML
```HTML
<div class="box">
  Content!
</div>
```
CSS
```CSS
.box::after{
content: "뒤!";
}
```
출력 : Content! 뒤!

5. 속성 선택자
속성 선택자는 HTML의 속성과 값으로 요소를 선택, **[]** 기호 사용

CSS에 HTML 속성 이름을 []기호 사이에 입력하면 비활성화된 요소 선택됨
```CSS
[disabled]{
  color: red;
}
```

CSS에 HTML의 type 속성을 포함한 요소를 선택하려면
```CSS
[type]{
  color: red;
}
```

비밀번호 입력 요소를 선택하려면 속성과 값을 한꺼번에 작성
```CSS
[type="password"]{
  color: red;
}
```

입력 요소의 값이 HELLO 인 값을 선택하려면 속성과 값을 한꺼번에 작성
```CSS
[value="HELLO"]{
  color: red;
}
```

# 스타일 상속
특정 class 요소의 하위 요소에 CSS 스타일을 상속시킬 수 있다.   
모든 CSS 속성이 하위 요소에 상속되는 것은 아니고 대부분 글자와 관련된 속성들이 상속 가능하다.

* font-style : 글자 기울기
* font-weight : 글자 두께
* font-size : 글자 크기
* line-height : 줄 높이
* font-family : 폰트
* color : 글자 색상
* text-align : 정렬

**강제 상속**    
height 강제 상속 예
[html]()
[css]()
