# HTML 핵심 요소

### 1. < div >
* div 태그는 블록 요소에 해당   
* 특별한 의미는 없고 구분을 위해 사용됨
ex) 중요한 내용이 담긴 곳을 구분할 때 사용하기도 함

### 2. < h1 >
* 블록 요소
* 제목을 의미하는 heading의 약어
* h1 태그 부터 h6 태그까지 총 6개 작성 가능 (h 뒤에 붙은 숫자가 작을수록 더 중요한 제목임을 의미함)

### 3. < p >
* 블록 요소
* 문장을 의미하는 paragraph의 약어
* 내부의 어떤 문장을 담아냄

### 4. < img >
* 이미지를 삽입하는 인라인 요소
* 삽입할 이미지의 경로와 이미지가 출력되지 못할 경우 대신해서 나타낼 텍스트 입력
```HTML
<img src="img/weather.jpg" alt ="12호 태풍"/>
```

### 5. < ul > , < li >
* ul : 순서가 필요없는 리스트
* ul은 li 태그를 무조건 자식 요소로 포함해야 함
* ul, li 모두 블록 요소이며 두 태그는 한 세트여서 둘 중 하나만 사용될 수 없다.

### 6. < a >
* anchor, 닻이라는 의미를 가짐
* 한 페이지에서 다른 페이지 혹은 같은 페이지로 이동하는 하이퍼링크를 지정할 때 사용하며 인라인 요소에 해당

```HTML
<a href="https://www.naver.com">NAVER</a>
<a href="https://www.google.com" target="_blank">Google</a>
```
* target 속성은 연결되는 링크가 어떤 브라우저 탭에서 열릴지를 지정
* _blank 값은 새로운 탭에서 링크의 페이지를 열겠다는 의미

### 7. < span >
* 특별한 의미 없이 단순한 텍스트 구분을 위해 사용되는 인라인 요소

ex) span 태그로 특정 글자에만 css 스타일 적용 가능
```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      span{
        color: red;
      }
    </style>
  </head>
  <body>
    <p>
      <span>동해물</span>과 백두산이 마르고 닳도록
    <p>
  </body>
</html>
```

### 8. < br >
* break의 약어로 **줄바꿈**을 할 수 있름

### 9. < input >
* 사용자에게 데이터를 입력받을 때 사용
* 인라인 요소지만 일부는 블록 요소의 특성을 가진 요소로 인라인-블록 요소라고 불림
* type 속성에는 사용자에게 입력 받을 데이터의 타입 지정
* 가로,세로 너비와 위,아래,좌,우 여백 지정 가능

* **일반 텍스트 사용 방법**   
```HTML
<input type="text"/>
```

* **값을 미리 입력하는 방법**
사용자에게 입력받을 값을 미리 넣어둠
```HTML
<input type="text" vaule-"HEROPY!"/>
```
<br</br>

* **사용자에게 입력값의 힌트를 주는 방법**      
사용자에게 어떤 값을 입력하면 좋을지 힌트
```HTML
<input type="text" placeholder="이릅을 입력하세요"/>
```

* **입력 요소를 비활성화하는 방법**
disabled 속성 추가하면 입력 요소에 값 입력 불가
```HTML
<input type="text" disabled />
```

* **체크박스 사용 방법**
```HTML
<label>
  <input type="checkbox"/>Apple
</label>
<label>
  <input type="checkbox"/>Banana
</label>
```
체크 박스 옆의 텍스트를 선택해도 체크가 가능하도록 label 태그 사용

checked라는 속성 사용하면 체크가 되어있는 상태로 화면에 출력

```HTML
<label>
  <input type="checkbox" checked/>Apple
</label>
```

* **라디오 버튼 사용 방법**

라디오 버튼은 하나만 선택 가능   
라디오 버튼을 만들 때는 각 입력에 name 속성 꼭 사용해야 함
```HTML
<label>
  <input type="radio" name="fruits" checked/>Apple
</label>
<label>
  <input type="radio" name="fruits"/>Banana
</label>
```

### 10. < table >
* 표를 만들 때 사용
* 행의 개수를 먼저 지정하고 각 행에서 열의 개수 지정

```HTML
<table>
  <tr>
    <td>A</td><td>B</td>
  </tr>
  <tr>
    <td>C</td><td>D</td>
  </tr>
<table>
```
출력
> A B
> C D


<br></br>

# 핵심 요소 출력
* [h1, img, ul, li 출력](https://github.com/gracelee5/Frontend_start/blob/main/Chapter5/chapter5_1.html)

* span, div, br 출력
우리나라만 빨간색으로 바꾸고 배경은 검정색으로 하기   
HTML   
```HTML
<p>
  동해물과 백두산이 마르고 닳도록
  하느님이 보우하사 <span>우리나라</span> 만세>
</p>
```
CSS
```CSS
body{
  font-size: 50px;
}
span{
  color: red;
  background: black;
}
```

* [input 출력](https://github.com/gracelee5/Frontend_start/blob/main/Chapter5/chapter5_2.html)

* table 출력
HTML
```HTML
<table>
  <tr>
    <td>A</td>
    <td>B</td>
    <td>B</td>
  </tr>
  <tr>
    <td>C</td>
    <td colspan="2">D</td>
  </tr>
</table>
```
colspan 입력된 칸이 두개의 열만큼 확장되며 세번째 열과 병합

CSS
```CSS
table{
  
}
tr{
  
}
td{
  border:1px solid red;
  padding: 10px ;
}
```
선 만들고 각 칸에 여백 추가


# 전역 속성
HTML의 모든 태그에 사용 가능한 속성
1. title
설명을 집어넣기를 원하는 태그에 title 속성을 작성하면 된다.
> < 태그 title="설명">< /태그 >

2. style
요소에 직접 스타일(CSS)을 적용하게 해주는 속성
> < 태그 style-"스타일">< /태그>

3. class
요소에 이름 지정해주는 속성
> < 태그 class-"이름">< /태그>

왜 요소에 이름을 쓰는가?   
수많은 글자에 여러 스타일을 적용할 때 구분이 없으면 특정 글자를 찾을 수 없음
```HTML
<span class-"blue">동해물</span>과 <span class="red">백두산</span>이 마르고 닳도록 하느님이 보우하사 <span class="red">우리나라 만세</span>
```

4. id
요소의 고유한 이름 지정   
class와 다른 점은 고유하다라는 것 -> 중복 불가

> < 태그 id="이름"></ 태그>

5. data
요소를 데이터에 저장하는 용도로 사용되는 전역 속성
> < 태그 data-이름-"데이터"></ 태그>

HTML
```HTML
<div data-fruit-name="apple">사과<div>
<div data-fruit-name="banana">바나나<div>
  ```
  
 JS
 ```JS
 const elements = document.querySelectorAll('div')
 elements.forEach(element=>{
 console.log(element.dataset.fruitName)
 })
 ```
 Console 탭에서
 apple과 banana가 출력된 것을 확인할 수 있다.
