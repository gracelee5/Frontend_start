# HTML 핵심 요소

1. < div >
* div 태그는 블록 요소에 해당   
* 특별한 의미는 없고 구분을 위해 사용됨
ex) 중요한 내용이 담긴 곳을 구분할 때 사용하기도 함

2. < h1 >
* 블록 요소
* 제목을 의미하는 heading의 약어
* h1 태그 부터 h6 태그까지 총 6개 작성 가능 (h 뒤에 붙은 숫자가 작을수록 더 중요한 제목임을 의미함)

3. < p >
* 블록 요소
* 문장을 의미하는 paragraph의 약어
* 내부의 어떤 문장을 담아냄

4. < img >
* 이미지를 삽입하는 인라인 요소
* 삽입할 이미지의 경로와 이미지가 출력되지 못할 경우 대신해서 나타낼 텍스트 입력
```HTML
<img src="img/weather.jpg" alt ="12호 태풍"/>
```

5. < ul > , < li >
* ul : 순서가 필요없는 리스트
* ul은 li 태그를 무조건 자식 요소로 포함해야 함
* ul, li 모두 블록 요소이며 두 태그는 한 세트여서 둘 중 하나만 사용될 수 없다.

6. < a >
* anchor, 닻이라는 의미를 가짐
* 한 페이지에서 다른 페이지 혹은 같은 페이지로 이동하는 하이퍼링크를 지정할 때 사용하며 인라인 요소에 해당

```HTML
<a href="https://www.naver.com">NAVER</a>
<a href="https://www.google.com" target="_blank">Google</a>
```
* target 속성은 연결되는 링크가 어떤 브라우저 탭에서 열릴지를 지정
* _blank 값은 새로운 탭에서 링크의 페이지를 열겠다는 의미

7. < span >
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

8. < br >
* break의 약어로 **줄바꿈**을 할 수 있름

9. < input >
* 
  
