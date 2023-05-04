# 기본 구조
```HTML
<h1>Hello HTML~<h1>
```
'<'로 시작해서 '>'로 끝나는 하나의 구조를 **태그**라고 부른다.   
태그와 태그 사이에는 내용이 들어간다.


# 부모-자식 관계
태그를 중첩하여 쓸 때 감싸고 있는 태그가 부모 요소이다.   
시각적으로 구분하기 쉽게 하기 위해 줄을 바꾸고 들여쓰기를 하는 것이 좋다
```HTML
<body>
  <div>
    <div></div>
  </div>
</body>
```
body 태그 바로 아래에 있는 div 태그는 body 태그의 자식 요소, 그보다 아래에 있는 div 태그는 body 태그의 하위(후손)요소. 자식 요소도 하위 요소에 포함된다.


# 빈 태그
열린 태그만 존재하고 닫힌 태그가 없는 태그
ex)
```HTML
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reset-css@5.0.1/reset.min.css"> 
<link rel="stylesheet" href="./main.css">
```
작성하는 방법
1. 열린태그만 작성
2. 열린 태그 뒤쪽에 / 붙이기   
ex)```<meta charset="UTF-8"/>```   
HTML5 버전에서는 두개 다 사용 가능하지만 혼용해서 쓰면 안 된다. 특수한 상황에서는 두번째 방법만 유효할 수도 있다.

# 속성과 값
태그에는 다양한 속성과 값을 적용할 수 있다.   
> <태그 속성="값">내용</태그>

**img 태그**
* 삽입할 이미지의 경로는 src 속성으로 작성
* 이미지 출력될 수 없는 경우 이미지 대체 텍스트는 alt 속성 다음에 작성
```HTML
<img src="./cat.jpg" alt="고양이"/>
```

**input 태그**
input 태그는 태그 이름과 사용자가 입력할 데이터 타입을 명시하는 type 속성으로 이루어져 있다.
```HTML
<input type="text"/>

<input type="checkbox"/>
```

# 글자와 상자
HTML 요소
* 글자 (인라인) : 글자를 다루기 위한 요소들
* 상자 (블록) : 상자(레이아웃)를 다루기 위한 요소들

## 글자(인라인 요소)   
대표적인 인라인 요소: < span >   
span 태그 : 본질적으로 아무것도 나타내지 않는 단순한 영역 설정용
```HTML
<span>Hello</span>
<span>World</span>
```
단순히 어디까지가 Hello이고 어디서부터 어디까지가 World인지 나타냄   
이 코드를 출력하면 Hello와 World가 띄어쓰기로 구분된 채 출력   
> Hello World

인라인 요소는 왼쪽에서 오른쪽으로 수평으로 쌓이는 특징이 있다.   
인라인 요소는 기본적으로 글자를 의미하는데 요소와 요소 사이를 줄바꿈하면 화면에서 한 칸 띄어쓰기로 나타난다

HTML
```HTML
<span>Hello</span>
<span>World</span>
```
CSS
```CSS
span{
  font-size:100px;
  }
```
-> 글자는 커졌지만 사이에 들어간 공백의 크기는 커지지 않음 (단어 사이가 비좁아짐)

비좁은 간격을 수정하려면?
CSS
```CSS
body{
  font-size:100px;
  }
```

참고) 인라인 요소는 글자를 다루는 요소이기 때문에 별도의 가로/세로 너비를 입력해도 그 내용이 브라우저에 출력되지 못한다.

## 상자(블록 요소)
대표적인 블록 요소 : < div >   
단순한 영역 설정용 

블록 요소는 요소가 **수직**으로 쌓이는 특징이 있다.

```HTML
<div>Hello</div>
<div>World</div>
```
출력
> Hello
> World

* 블록 요소는 부모 요소의 가로 너비만큼 최대한 늘어나려는 성질이 있고 세로 길이는 최대한 줄어즐려는 성질이 있다.   
* 블록 요소는 가로/세로 너비를 지정할 수 있다.
```HTML
<div style="width: 100px;">Hello</div>
<div style="height: 40px;">World</div>
```

* 요소의 여백도 자유롭게 지정이 가능하다
외부 여백을 지정하는 **margin** 속성과 내부 여백을 지정하는 **padding** 속성을 통해 지정 가능
```HTML
<div style="margin: 10px;">Hello</div>
<div style="padding: 10px;">World</div>
```

* 블록 요소는 자식 요소를 포함하는 데 제한이 없어 인라인 요소도 자식 요소로 품을 수 있다.
