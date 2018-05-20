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


## 20180518 

<BE - 개발 설정하기 >
- java coding convention - 구글꺼 번역해서 정리해볼까?

- 프로젝트명, 패키지명 - 소문자로 
- 클래스명 - 대문자로 

<tomcat 설치하기>

- WAS > Apache의 Tomcat : 웹 어플리케이션 실행 위해 필요하다. 
WAS 란 무엇인가? 

-tomcat 설치 후 
127.0.0.1: 8080 들어갔는데 로그인하라고함.. 
찾아보니 

<!--
  <role rolename="tomcat"/>
  <role rolename="role1"/>
  <user username="tomcat" password="<must-be-changed>" roles="tomcat"/>
  <user username="both" password="<must-be-changed>" roles="tomcat,role1"/>
  <user username="role1" password="<must-be-changed>" roles="role1"/>
-->
//여기에 이 두줄을 추가해줘 권한을 설정한다. 
   <role rolename="manager-gui"/>
  <user username="admin" password="admin" roles="manager-gui"/>

</tomcat-users>

출처 - https://www.mkyong.com/tomcat/tomcat-default-administrator-password/

role은 아래에 보면 여러가지가 있다. 

1) manager-gui — Access to the HTML interface.
2) manager-status — Access to the "Server Status" page only.
3) manager-script — Access to the tools-friendly plain text interface that is described in this 4) document, and to the "Server Status" page.
5) manager-jmx — Access to JMX proxy interface and to the "Server Status" page.

출처 - tomcat.apache.org

 
## 20180519

<Servlet 이란?>

-자바 웹 어플리케이션 : html css 이미지 서블릿 jsp.. 이 구성으로 포함될 수 있다. 여러개 포함 될 수 있다. 

웹 어플리케이션은 was같은 미들웨어를 통해 실행한다 .
내가 몽땅 전부 하는게 아니라 이처럼 was를 통해 만든다면 그에 따른 규약을 따라야한다. 

그 약속중 하나인 <자바 웹 어플리케이션의 폴더 구조> ! 이 폴더 구조를 따라야한다. 
-xml 파일 : 배포 기술자. 웹어플리ㅔ이션의 관한 정보를 다 가진 파일이라 보면된다. 
 서블릿 3.0 미만은 필수, 3.0은 어노테이션이 역할을 대신한다. 

-classes 폴더에 서블릿 파일이 위치.


-서블릿이란 : 자바 웹 어플리케이션의 구성요소 중 동적인 처리 하는 프로그램의 역할 

-서블릿은  was에서 동작하는 java 클래스이다. 
-서블릿은 HttpServlet 클래스를 상속받아야한다.
-서블릿과 JSP로부터 최상의 결과를 얻으려면, 웹 페이지를 개발할 때 이두가지(jsp , 서블릿)을 조화롭게 사용해야 한다. 


<Servlet 작성 방법>

방법 1) servlet 3.0 이상에서 사용하는 방법 
- 자바 어노테이션을 사용한다. 

방법 2) servlet 3.0 이하에서 사용하는 방법
- 서블릿 등록시 xml파일에 직접 등록한다. 

실습1 - 방법1 
새 프젝 생성할 때 다이나믹프젝버전을 눈여겨보자. 
마지막에 xml

요청이 들어왔을 때 이 서블릿이 실행되면서 응답할 코드를 만들어내고 
만들어 낸 코드로 응답을 하는 것이다 -> 동적 페이지 

서버는 요청을 받아내는 객체와 응답을 하는 객체를 만들어낸다. 
response 객체에다가 넣는 받을 객체가 무슨 타입인지 알아야 해서 .setContentType()씀. 
-> 응답 보낼 내용 앤드 보내는 응답의 타입 
그다음 무슨 내용으로 보낼 것이냐. 출력 메서드 객체 어쩌구 써서 한다...
tip html 은 br을 넣어야 엔터가 되기때문에 print()를 쓰든 println()을 쓰든 노상관 .

+) 자바 어노테이션이란??


실습2 - 방법2
-과정-
 
url /Ten 이라고 요청 들어와서 있으면 
xml에서 servlet-name 을 확인하고 
<servlet>부분에서 display-name과 맞는 애를 찾고 servlet-class , 내가 실행 할 애가 누구지?하고 확인하는 것이다. 

url 바꾸고 싶으면 xml파일 url-pattern 부분을 바꾸면 된다. 


<서블릿의 생명주기>
system.out은 콘솔에 보내줘요 
print.out은 다른데다 보내느 거 . 


요청이 객체가 메모리에 있나 없나? 있으면 서비스만 호출된다. 
없으면 LifecycleServlet 객체 생성하고  init()생성하고 서비스 호출 
destroy 는 was가 종료되거나 웹 앱이 갱신 될 경우 호출된다. 

doPost ,, doGet ,,
 
<Requset, Response>
- HttpServletRequest 객체
- HttpServletResponse 객체

--------------------------------------------

<less compile 하기>

노드.. 
걸프 -미들도구 를 이용해서 

<transition을 이용한 css 기본 애니메이션>
트랜지션  : 박스 엘리먼트가 움직일 속도를 조정해서 애니메이션 효과를 주는 
css에 속성으로 선언한다.  구글링해서 참고하면서 작성해보잣 

<transform 속성 활용>
transform : 이 속성을 이용해서 다른 엘리먼트에 영향을 미치지 않고 특정 엘리먼트의 위치를 바꿀 수 있다. 
translate 속성 추가하면 빠른 속도로 렌더링이 되는듯?


대체로 translate3d속성을 많이 쓴다. 


## 20180520

- head와 header 태그 차이 
head는 구조적으로.. 서문같은 거다 
나타나게 하는 그런게아니었다 

- 시맨틱 태그의 중요성 , html 구조의 중요성

-배치의 이해 중요하다..
 layout작업 = renderin 과정 = 배치 : 엘리먼트를 화면에 배치하는 작업
[배치 관련 속성]
1. display [block : 위에서 아래로 쌓이는 형태 / inline : 수평으로 ]
2. position 
- static
- absolute : static 아닌 값을 기준점으로. 아닌거 찾기 위해 위로위로 올라간다.
top~bottom 으로 설정한다. 설정시 top, left값은 0을 주더라도 꼭 설정한다. 
- relative : 원래 자신이 위치해야할 곳 기준. top~bottom 으로 설정한다.
- fixed : 스크롤 안따르고 그냥 박혀있게 
-float


<box-sizing>
-padding 적용시 박스 크기 안변하게 하고 싶을때 

<box-shadow>
box-shadow:[inset] (오른쪽위치) (아래위치) (블러) (색상);

출처: http://dolly77.tistory.com/11 [interactive]








 
 
 
 
 
