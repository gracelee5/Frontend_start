# JS 개요

1. 표기법    
  **dash-case**  
   -로 단어와 단어 사이 연결 (HTML, CSS)

  **snake_case**   
  _로 단어와 단어 사이 연결 (HTML, CSS)

  **camelCase**
  단어의 첫 글자 대문자로 첫번째 단어의 첫 글자는 소문자로(JS)

  **PascalCase**
  단어의 첫 글자 대문자로 첫번째 단어의 첫 글자도 대문자로(JS)

2. 주석
   ``` // 한 줄 주석
       /*한 줄 주석*/
       /**
       *여러 줄
       *주석
       */
   ```

# 데이터 종류
1. String    
   "", '', `` 와 함께 표기

2. Number    
   정수 및 부동소수점을 가진 숫자를 이용하여 표현

3. Boolean    
   true, false 두 가지 값으로 구분됨

4. undefined    
   아무것도 정의되지 않은 상태, JS에서는 데이터를 직접 할당하지 않으면, 자동으로 undefined 할당

5. null    
   의도적으로 비어있음을 나타냄

6. Object    
   Ket-Value 형태로 여러 가지 데이터 저장

7. Array     
   여러 데이터를 순차적으로 나열하여 저장, 대괄호 이용 []

# 변수
1. const : 재할당 불가    
2. let : 재할당 가능   

# 함수 
1. 함수의 선언과 호출     
   function라는 키워드로 선언할 수 있음
   ```JS
   function helloFunc(){
     console.log(1234);
   }
   //함수 호출
   helloFunc();//1234
   ```

2. 함수의 데이터 반환    
   함수 내부에서 return이라는 키워드를 사용하면 데이터가 반환되며 함수가 종료된다.

3. 선언된 함수 재사용     
   선언된 함수는 유효한 범위 내에서 재사용 가능하다.

4. 기명 함수와 익명 함수
   ```JS
   //기명 함수
   function hello(){
     console.log("Hello~");
   }
   hello();

   //익명 함수
   const world = function(){
     console.log("World~");
   }
   world();
   ```
   익명 함수는 변수에 할당하지 않으면 재사용할 수 없음

# 조건문
1. if 조건문    
   참과 같은 값이면 코드 블록 실행
   ```
   const isShow = true;
   const checked = false;

   if (isShow){
    console.log('Show!');//Show!
   }

   if (checked){
    console.log('Checked!');
   }
   ```

2. if else 조건문    
   조건에 따라 실행할 코드 블록 나눔
   ```
   const isShow = true;

   if (isShow){
    console.log('Show!');//Show!
   }else{
    console.log('Hide?');
   }
   ```

# DOM API
JS에서 HTML을 제어할 수 있는 명령들   
1. 실습 1
   <script> 작성 위치에 따라 동작 여부가 결정    
   
```HTML
<script src="./main.js"></script>
```
를 body에 넣음 [1](https://github.com/gracelee5/Frontend_start/blob/main/Chapter8/%EC%8B%A4%EC%8A%B51/index1.html)      
or    
<script>위치를 이동시키지 않고 defer 속성 추가
```HTML
<script defer src="./main.js"></script>
```
[2]https://github.com/gracelee5/Frontend_start/blob/main/Chapter8/%EC%8B%A4%EC%8A%B51/index2.html


2. 실습2
JS로 요소를 클릭했을 때 동작하는 코드
HTML 코드는 같음
[JS](https://github.com/gracelee5/Frontend_start/blob/main/Chapter8/%EC%8B%A4%EC%8A%B52/main.js)

3. 실습3
JS에서 HTML class 속성 제어      
**classList** 속성 사용
