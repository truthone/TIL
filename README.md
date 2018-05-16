# Today I Learned
Today 

## 20180511
### edwith - html & CSS
### ch.1 html을 통한 웹사이트 구조 설계 

#### HTML 이란?
- HTML 전문 개발자 = markup 개발자 
- HTML 이란? Markup 언어(다양한 정보를 쉽게 표현하기 위한 포맷)
- 기본 형태 : head , body 
- 태그 & 속성값 

#### HTML의 중요 태그들 
- w3schools.com 에서 확인 가능

 'title'
 'h1 ,h2...'
 'ul : unordered list' 
 'li : 리스트'
 'a : 닻을 내린다 , href : 속성으로 url.' 
 
 ## 20180512
 
 #### UI레이아웃 위한  html 태그
 - 기본적으로 header footer 본문 영역
 - footer : div랑 같은 역할을 함. html5부터 생긴 태그
 - nav : navigation 
 - header, footer.. 적용안되는 하위 버전은 'div = header' 이런식으로 쓰기도 한다. 
 - aside / section ...
 
 *div를 남용 하는 것은 안좋고, 협업 시 동료들과 협의해서 태그 뭘 쓸지를 정한다. 
 *구조화 설계 !
 
 #### Id & class
 - class를 지정해 같은 class인 것들의 스타일을 다같이 수정 할 수 있다. 
 - id = 고유값을 지정해 찾을 때 유용하게 한다. 
 
 ## 20180515
 #### Web 개발의 이해 - Front-end & Back-end
 1) 웹 프로그래밍을 위한 프로그램 언어들 
 - kotlin : JVM 기반으로 java와 상호 운영 100%. 현대 프밍 언어의 발전을 대다수 계승한 모던 프로그래밍 
 
 - 깃헙에서 가장 인기 있는 프밍언어 : 1위 - 자바스크립 / 2위 - 파이썬 / 3위 - 자바 
 
  <웹 관련 인기 언어>
 - 파이썬 - 배우기 쉽다. 데이터 과학 , 웹개발에도 자주 쓰임 
 - PHP - 웹의 80% 이상은 php
 - javascript, java , ruby - 빠른 개발. 단순세련된 웹어플리케이션 만들 수 있다. 
 
 2) 웹동작 - HTTP 프로토콜의 이해 
 
 ## 20180516
 #### css 기본 
 
 font- size : -em -> 부모폰트값의 배수로 설정하는 방법 

padding : -px (위) (아래) (왼) (오) ; 또는 padding-bottom : 이런식으로 할 수 있다. 

margin 도 마찬가지 

margin : element 간 간격 

인저한 두 개의 block  element가 서로 다른 margin을 가지고 있다면 
-> 큰 값 가진 마진값이 공유되어 사용된다 

인접한 두개의 inline element의 margin은?
-> 각 마진의 합으로 표현 

마진의 다양한 축약 표기벗 

<position> 

static 
relative : top, left값 기준으로 상대적으로  움직임 . top: 40px left: 40px -> 위에어서부터 40 .. 
absolute  : 자신의 기준점이 static이 아닌 애를 기준점으로 한다. 자기 부모중 static아닌 놈으로 계속 타고 올라간다. 

fixed : 스크롤이 생길때 움직이지 않는다. 


* 부모기준으로 정렬하고 싶다면 , 부모 속성을 rerlative를 주고 시작하면 자식이 absolute일때 기준으로 삼기 쉽게 작성할 수 있다. 
-> absolute는 static '아닌' 애를 찾아서 기준으로 삼기 때문이다. 

<float 속성이란>
float: left || right; 
lfloat -> float 해제 

-글과 그림이나 위치 조정이나  레이아웃 배치에서 사용한다.

-레이아웃 좌우로 배치 할 때 쓴다. 
위로 뜨고 float 끼리는 겹치지 않기 때문..  
-margin 으로 조정한다. 

-원래 기본적으로 아래로아래로 배치 되는데, 
float을 쓰면 수평으로 배치되는 효과!

---

[float 때문에 생기는 문제점 앤드 해결방법] -> 실습통해 익숙하게, 외우자 !

- 하위 엘리먼트에 float을 주었을 경우, 상위 엘리먼트의 overflow를 줘야한다.
- float 준 자식 컨테츠가 부모 안에 안들어갈때 
overflow : auto || hidden
부모에 overflow 속성을 해줘야 
float 로 돼있는 자식들을 인정해준다 

- 위에 있는 float 를 인정ㅎ
clear : left || right || both -> float :left 나 float : right 아님 둘다.. 속성을 clear (없애고) 인식하겠다 : 위에 뭐가 있다 인식돼서 안겹침. 
위 속성에 clear 속성 써주면 된다. 

<FLEX 기반 layout>
flex : 웹페이지 만들 때 레리아웃을 쉽게 만들수 있도록 도와주는 css속성이다. 

브라우저는 제약있어서 사용 어렵긴 하지만 모바일웹에서 확인을 해보자 
-반응형 웹을 구현 할 때 flex를 주로 사용한다. 

컨테이너 flex / 아이템 flex 
- 구글 검색 : a complete guide to flexbox  참고해서 작성해보자 
 
<z-index 속성의 이해>
static 값이 아닌 녀석끼린 겹칠 수 있는데 겹친 순서를 어케 할 것이냐
원래는 나중에 선언된애가 위로 오는건데 이 순서를 바꿀 수 있다 z-index를 이용해서!!! 

z-index : 값 
큰 값 순서에 따라 위로 온다. 
단 부모가 값이 작으면 자식이 아무리 커도 위로 못감 ㅠ
값 올려도 왜 안올라올까 ㅠㅠ 하면 부모값을 살펴보자 
-  >stacking context 


<LESS>
css의 단점들... 
색깔 맞추는 컨셉으로 가고 있는데 하나 바꿀라면 하나하나 다 바꿔야하는.. 
.. 순서 찾기 , 

1. variables :  변수가 없다 
2. mixins : 이미 선언된 클래스를 재활용해서 사용하고 싶을때 
3. 중첩된 룰처리 : 
3. peration : 연산도 안되고 

LESS를 사용하게 되면 프로그램적인 작성이 가능해진다. 
하지만 정식지원이 안되기 때문에 less로 작성후 css로 변환해서 배포 .

@base_wdth : 300px -> 변수처럼 선언 

.content ; -> 속성안에 설정하면 content속성 가져온다 
근데 뭐 마진값만 바꾸고 싶다 하면 밑에 바로 써주면 된다. 

ex) content설정 여기저기 있는걸 모으고 싶다 하면 
.contnet {
  li {   -> 이런 식으로 함수 안 함수 처럼 
       a {
           }
   }
 } 

+) less 컴파일 


 
 
 
 
 
