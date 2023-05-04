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
