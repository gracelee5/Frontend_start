# Codepen.io
기존에 작업했던 프로젝트는 그대로 두고 새로운 내용 테스트할 때 도움이 된다.

[Codepen.io](https://codepen.io/)

별도의 저장 없이 즉시 결과가 뷰포트에 나타난다.

# 브라우저 스타일 초기화
웹사이트가 브라우저 종류와 상관없이 같은 모습으로 보이길 원한다면 각 브라우저에서 제공하는 기본적인 CSS 스타일을 초기화해야 한다.

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./main.css">
</head>
<body>
    <div></div>
</body>
</html>
```

```CSS
div{
    width: 200px;
    height: 100px;
    background-color: orange;
}
```
이렇게 작성했을 때는 요소의 위와 좌측에 여백이 생긴다. 이 여백을 없애려면

## CDN
link 태그에 다음 코드를 붙여 넣는다
```HTML
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reset-css@5.0.1/reset.min.css"> 
```

## Codepen.io에 적용
1. CSS 패널의 톱니바퀴 아이콘 클릭
2. CSS Base 옵션을 Reset에 체크 후 
