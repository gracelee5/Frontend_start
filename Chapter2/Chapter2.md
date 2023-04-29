
VScode에서 html 파일을 생성하고 느낌표를 입력하면 자동 완성 메뉴가 나타나는데 엔터를 치면 기본적인 HTML 구조가 나타난다.


## 코드의 구조와 역할
< !DOCTYPE html > : 문서의 HTML 버전 지정   

< html > : HTML 문서가 어디에서 시작되어 어디에서 끝나는지 브라우저에게 알려줌 (문서의 전체 범위 나타냄)   

< head > : 문서의 정보를 나타내는 범위, 브라우저가 해석해야 할 웹페이지의 제목과 설명, 파일의 위치, 스타일(CSS)과 같은 눈에 보이지 않는 정보가 들어감   

< body > : 문서의 구조를 나타내는 범위, 사용자 화면에 나타나는 로고, 헤더, 푸터, 내비게이션, 메뉴, 버튼, 이미지와 같이 우리가 눈으로 볼 수 있는 구조의 대한 정보가 이 안에 들어감

## HTML, CSS, JS 연결하기

**HTML, CSS 연결**   
1. html파일의 title 태그 다음에 한 행을 추가한다.
2. link 라고 입력하고 Tab 누르면 href 속성을 포함한 link 태그가 만들어진다.
3. href 속성에서 "" 사이에 ./main.css라고 입력한다.
```
<link rel="stylesheet" href="./main.css">
```

index.html 파일의 lang 속성을 ko로 바꿔주면 번역 팝업이 나타나지 않는다.   
```
<html lang="ko">
```

**HTML, JS 연결**   
1. script 입력 후 tab키 누름
2. script 태그 안에 src 속성 추가 후 "" 안에 ./main.js 입력.  
```
<script src="./main.js"></script>
```
3. 개발자 도구 열어서 Console 탭을 클릭하면 main.js 파일에 입력했던 HEROPY! 라는 단어가 출력된 게 보인다. 

**개발자 도구 여는 법**   
* 오른쪽 위 점 세개 누른 후 -> 도구 더보기 -> 개발자 도구


## 태그   
1. < title > : HTML 문서의 제목을 정의, 실제 브라우저 탭에 표시

2. < link > : 외부에 있는 문서를 가져와 연결할 때 사용하는 태그, 주로 CSS 파일을 가져와 연결할 때 사용   
  href 속성에는 가져올 문서의 경로 표시, 전부 ./로 시작(./는 현재 html 파일의 주변 경로를 의미)   
  rel 속성에는 가져올 문서와 현재 파일의 관계를 적음   
```
<link rel="stylesheet" href="./main.css">
<link rel="icon" href="./favicon.png">
```

3. < style > : CSS와 관련된 내용을 HTML 문서 안에 직접 사용할 때 사용
```
<style>
  div {
    color: red;
  }
```

4. < script > : 외부의 JS 파일을 가져와 HTML 파일에 연결할 때 사용, style 태그처럼 JS 내용을 HTML 문서 안에 직접 작성하는 용도로도 사용가능
```
<script src="./main.js"></script> //JS 파일을 직접 가져오는 경우
<script>
  console.log('hello world!')
</script> //JS를 HTML 문서 안에서 작성하는 경우
```

5. < meta > : HTML 문서의 제작자, 설명, 키워드 같은 여러 가지 정보를 검색엔진이나 브라우저에 제공
```
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
   
## 상대 경로와 절대 경로
### 상대 경로
