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

# 넘침 제어
overflow 속성은 내용이 요소의 크기 이상으로 넘칠 때, 보여지는 것을 제어함   
넘침 제어의 기본 값은 visible로 넘친 내용을 그대로 보여준다
* visible : 넘친 내용을 그대로 보여줌
* hidden : 넘친 내용을 잘라냄
* scroll : 넘친 내용을 잘라내고 스크롤바 생성
* auto : 넘친 내용이 있는 경우에만 잘라내고 스크롤바 생성

# 출력 특성
요소의 화면 출력 특성은 display 속성으로 제어
* 각 요소에 지정되어 있는 값
- block : 상자 요소
- inline : 글자 요소
- inline-block : 글자+상자 요소

* 따로 지정해서 사용하는 값
- flex : 1차원 레이아웃
- grid : 2차원 레이아웃
- none : 보여짐 특성 없음, 화면에서 사라짐

* 기타
- table, table-row, table cell 등

# 투명도
opacity 속성으로 요소의 투명도 지정, 기본값은 1이고 불투명함을 의미
> opacity: 0.4; 40% 불투명
> opacity: 0; 100%투명함

# 글꼴
* font-style : 글꼴의 기울기
normal, italic, oblique
* font-weight : 글꼴 두께
normal, bold, bolder, lighter, 100~900
* font-size : 글꼴 크기
일반 단위(px,em,rem), %(부모 요소 글꼴 크기의 백분율), smaller,larger(부모 요소보다 작게,크게
* line-height : 한 줄의 높이
숫자(요소 글꼴 크기의 배수), 일반 단위, %
* font-family  글꼴 이름

# 배경
background-로 시작되는 속성을 이용하여 요소 배경에 색상이나 이미지 추가 가능
1. background-color
  요소의 배경 색상 지정
  
2. background-image
  요소에 배경이미지 삽입
  ```CSS
  background-image: url("경로");
  ```

3. background-repeat
  요소 배경 이미지의 반복   
  repeat-x : 수평 반복
  repeat-y : 수직 반복
  no-repeat : 반복 없음
  
4. background-position
  요소 배경 이미지의 위치 지정   
  top, bottom, left, right, center의 각 방향을 지정하거나 단위로 정확한 위치 지정

5. background-size
  요소 배경 이미지의 크기 지정
  
6. background-attachment
  요소 배경 이미지의 스크롤 특성 지정 (scroll, fixed, local(요소 내 스크롤 시 이미지가 같이 스크롤)
  
# 배치
1. position
  요소의 위치를 지정하는 것이 아니라 위치 기준 지정   
  기본값 : **static** -> 위치 기준 없음   
  **relative**(요소 자신을 기준), **absolute**(위치상 부모 요소를 기준), **fixed**(뷰포트 기준), **sticky**(스크롤 영역 기준)

2. top, bottom, left, right
  요소의 실제 위치 지정, 기본값은 auto(위치값 없음)

3. 기준에 대한 이해
   **relative**
   요소들을 자기 자신 기준으로 배치 (원래 자신이 있던 위치 기준으로 배치해야 하기 때문에 실제로는 움직이지 않음, 화면에 보이는 위치만 달라짐)

   **absolute**   
   요소들을 부모 요소(해당 배치 요소의 상위 요소 중 position 속성의 갑(static 제외)이 존대하는 가장 가까운 요소) 기준으로 배치

   **fixed 값**   
   뷰포트를 기준으로 요소 배치, 화면을 스크롤해도 해당 요소의 위치가 고정 (최상단으로 이동하는 버튼)

# 플렉스
1차원 레이아웃을 만드는 기술 (수평축으로만 정렬하거나 수직축으로만 정렬하는 방법)   
Flex Container: 정렬할 요소들의 묶음   
Flex Items : 정렬할 요소

1. display
   요소의 화면 출력을 지정, flex 값을 적용하면 요소가 Flex Container로 정의, 해당 요소의 자식 요소들은 Flex Items로 정의   
   inline-flex 적용하면 Flex Container가 인라인 요소의 특징을 가짐 (하나의 Flex Container가 글자처럼 취급)

2. flex-direction
   Flex Container의 주축의 방향을 지정해주는 속성, 기본값은 row(행축, 수평) (column : 열축, 수직)
   row-reverse, column-reverse : 반대로 정렬

3. flex-wrap
   Flex Items의 줄바꿈 여부를 지정하는 속성
   기본값 : nowrap -> 한 줄로만 정렬하고, 정렬할 자리가 모자라면 Flex Items의 너비가 자동으로 줄어듦   
   wrap 값을 지정할 경우 Flex Items를 정렬할 자리가 모자라면 자동으로 줄바꿈

4. justify-content
   Flex Container 주축의 정렬 방법 지정  
   기본값 : flex-start (Flex Items을 시작점으로 정렬)
   그 외에도 flex-end, center 등의 값을 사용할 수 있음

5. align-content
   Flex Container 교차축의 정렬 방법을 지정
   기본값 : stretch (flex-start,end,center등의 값 지정 가능)   
   요소가 딱 한 줄만 있는 경우에는 사용할 수 없음

6. align-items
   Flex Container 교차축의 정렬 방법을 지정 다른 점은 한 줄에서의 정렬 방법을 지정

7. order
   Flex Items의 순서를 지정
   음수 사용 허용, 지정된 숫자가 클수록 순서가 뒤로 밀리는 성질이 있음

8. flex-grow
   Flex Items의 증가 너비 비율 지정   
   단위 사용 X, width 속성을 통해 요소의 가로 너비를 지정해둔다고 해도 flex-grow 속성으로 증가 너비 비율 지정하는 순간 요소의 너비가 늘어남

9. flex-shrink
   Flex Items의 감소 너비 비율 지정, 기본값 : 1
   감소 너비 비율을 0으로 지정하면 너비가 감소 안 됨

10. flex-basis
   Flex Items 공간이 배분되기 전의 기본 너비를 지정   
   기본값 : auto 요소 내용의 너비를 기본 너비로 사용   
   값을 0으로 지정하여 기본 너비가 없도록 만들 수도 있음

# 전환
> transition: 속성 지속시간 타이밍함수 대기시간;

* transition-property : 효과를 적용할 CSS 속성 이름 (기본값 :all)
* transition-duration : 효과가 지속될 시간을 지정 (기본값 :0s)
* transition-timing-function : 효과의 타이밍 함수를 지정 (기본값 :ease) (linear:일정하게, ease:느리게-빠르게-느리게, ease-in:느리게-빠르게, ease-out:빠르게-느리게, ease-in-out:느리게-빠르게-느리게)
* transition-delay : 효과가 몇 초 뒤에 시작할지 대기시간 설정(기본값 :0s)


# 변환
1. transform
   >transform: 변환함수1 변환함수2 변환함수3 ...;
   >transform: 원근법 이동 크기 회전 기울임;
   
2. perspective
   하위 요소를 관찰하는 원근 거리 지정
   
   perspective 속성과 함수의 차기   
   속성의 적용 대상 ; 관찰 대상의 부모, 함수의 적용 대상 : 관찰 대상

3. backface-visibility
   3D 변환으로 회전된 요소의 뒷면 표시 여부를 지정   
   기본값 : visible
   hidden으로 지정하면 요소를 180도 회전해도 뒷면이 화면에 보이지 않음
