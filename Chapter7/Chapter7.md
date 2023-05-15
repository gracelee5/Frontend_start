# CSS 속성 개요
1. 박스 모델   
HTML의 기본 요소를 만드는 여러 속성 (가로/세로 너비, 내부/외부 여백 등)
2. 글꼴, 문자
3. 배경
4. 배치
특정 요소를 원하는 위치에 가져다 놓은 것
5. 플렉스
수평 레이아웃을 만들 때 사용
6. 전환
요소의 전과 후의 변환 과정을 자연스럽게 애니메이션으로 처리
7. 변환
요소를 회전 및 이동 시키거나 크기 조절
8. 띄움   
요소를 공중에 띄우는 것    
ex) 신문 기사에 사진 주변에 있는 글자들
9. 애니메이션   
전환보다 버 복잡한 애니메이션
10. 그리드   
행과 열의 2차원 레이아웃을 만드는 데 사용
11. 다단   
하나의 페이지를 여러 개의 단으로 나눔
12. 필터

# 너비
1. width, height   
가로/세로 너비 지정해주는 속성, px나 % 단위 사용     
기본 값은 자동으로 계산 및 적용
2. max-width,max-height   
기본값은 none으로 최대 크기에 제한 없음을 나타냄   
3. min-width,min-height   
기본값 0

# 외부 여백
요소의 외주 여백은 margin 속성으로 지정   
margin 값은 음수를 가질 수 있다.

margin에서는 1~4개의 값을 순서대로 적어서 요소의 외부 여백을 지정할 수 있다.
> margin 0; - 모든 방향이 0
> margin 10px; - 모든 방향이 10px
> margin 10px 20px; - (수직, 수평) top, bottom = 10px, left, right = 20px
> margin 10px 20px 30px; - (상, 중, 하) top = 10px, left, right = 20px, bottom = 30px
> margin 10px 20px 30px 40px; - (시계 방향) top = 10px, right = 20px, bottom = 30px. left = 40px

# 내부 여백
요소의 내부 여백은 padding 속성으로 지정   
기본값은 0으로 음수 사용 불가

padding 속성은 요소 내부에 여백을 추가하는 속성이기 때문에, 요소의 크기가 지정한 가로/세로 값보다 커진다.   
만약 자신이 지정한 가로/세로 너비를 유지하면서 내부 여백이 추가되길 원한다면, 요소에 **box-sizing: border-box;** 속성과 값을 추가하면 된다.

padding 속성의 해석 방법은 margin과 같다.


# 테두리선
```CSS
border: 두께 종류 색상;
```

* border-width
  선의 두께를 지정하는 속성, 기본값은 medium
* border-style
  선의 종류를 지정하는 속성, 기본값은 none   
  soild, dashed, dotted, double, groovw, ridge, inset, outset
* border-color
  선의 색상 지정, 아무 색상도 지정하지 않으면 요소의 글자 색상 적용
  
# 모서리
border-radius 속성을 이용하여 요소의 모서리를 둥글게 처리할 수 있다.   
border-radius = 10px; -> 반지름이 10px인 원이 모서리 쪽에 생김

# 크기 계산
bow-sizing 속성은 요소가 가진 가로/세로 너비의 계산 기준을 지정, 기본값은 content-box

>content-box : 요소의 내용만 너비로 계산
>border-box : 요소의 내용 + padding + border 모두 너비로 계산

