
*180511*

## ch.1 html을 통한 웹사이트 구조 설계 

#### HTML 이란??
- HTML 전문 개발자 = markup 개발자 
- HTML 이란? Markup 언어(다양한 정보를 쉽게 표현하기 위한 포맷)
- 기본 형태 : head , body 
- 태그 & 속성값 

#### HTML의 중요 태그들 
- w3schools.com 에서 확인 가능
 ```
 'title'
 'h1 ,h2...'
 'ul : unordered list' 
 'li : 리스트'
 'a : 닻을 내린다 , href : 속성으로 url.' 
 ```
 ---
 
*180512*
 
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
 
 - class selector : .클래스 이름
 class = "클래스 이름"
 
 - id selector : # 아이디
 id = "id값"
 
 ---
 
*180515*
 
 ### Web 개발의 이해 - Front-end & Back-end
 
 ##### 웹 프로그래밍을 위한 프로그램 언어들 
 - kotlin : JVM 기반으로 java와 상호 운영 100%. 현대 프밍 언어의 발전을 대다수 계승한 모던 프로그래밍 
 
 - 깃헙에서 가장 인기 있는 프밍언어 : 1위 - 자바스크립 / 2위 - 파이썬 / 3위 - 자바 
 
  <웹 관련 인기 언어>
 - 파이썬 - 배우기 쉽다. 데이터 과학 , 웹개발에도 자주 쓰임 
 - PHP - 웹의 80% 이상은 php
 - javascript, java , ruby - 빠른 개발. 단순세련된 웹어플리케이션 만들 수 있다. 
 
 웹동작 - HTTP 프로토콜의 이해 

--- 

*180516*
## css 기본 
 
- font- size : -em -> 부모폰트값의 배수로 설정하는 방법 
- padding : -px (위) (아래) (왼) (오) ; 또는 padding-bottom : 이런식으로 할 수 있다. 
- margin 도 마찬가지 
- margin : element 간 간격 

Q. 인접한 두 개의 block  element가 서로 다른 margin을 가지고 있다면 
-> 큰 값 가진 마진값이 공유되어 사용된다 

Q. 인접한 두개의 inline element의 margin은?
-> 각 마진의 합으로 표현 
 
---
#### position

- static 
- relative : top, left값 기준으로 상대적으로  움직임 . top: 40px left: 40px -> 위에어서부터 40 .. 
- absolute  : 자신의 기준점이 static이 아닌 애를 기준점으로 한다. 자기 부모중 static아닌 놈으로 계속 타고 올라간다. 
- fixed : 스크롤이 생길때 움직이지 않는다. 


tip 부모기준으로 정렬하고 싶다면 , 부모 속성을 rerlative를 주고 시작하면 자식이 absolute일때 기준으로 삼기 쉽게 작성할 수 있다. 
-> absolute는 static이 '아닌' 애를 찾아서 기준으로 삼기 때문이다. 

---
---
#### float 속성이란

 float: left || right; 
- lfloat -> float 해제 

- 글과 그림이나 위치 조정이나  레이아웃 배치에서 사용한다.
- 레이아웃 좌우로 배치 할 때 쓴다. 위로 뜨고 float 끼리는 겹치지 않기 때문..  
- margin 으로 조정한다. 
- 원래 기본적으로 아래로아래로 배치 되는데, float을 쓰면 수평으로 배치되는 효과!

```
[float 때문에 생기는 문제점 앤드 해결방법] -> 실습통해 익숙하게, 외우자 !

Q. float 준 자식 컨테츠가 부모 안에 안 들어갈 때  
--> 하위 엘리먼트에 float을 주었을 경우, 상위 엘리먼트에 overflow를 써줘야 
하위 엘리먼트들이 상위 엘리먼트 안으로 들어간다. (겹쳐진다.)
**overflow : auto || hidden**

-clear
속성을 clear (없애고) 인식하겠다 --> 위에 뭐가 있는 것처럼 인식돼서 안겹침. 
위 속성에 clear 속성 써주면 된다. 
**clear : left || right || both**
```
---
---
#### FLEX 기반 layout
flex : 웹페이지 만들 때 레이아웃을 쉽게 만들 수 있도록 도와주는 css속성.

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
---

---
#### LESS
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

---
---

*180518* 

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

 
*20180519*

## Servlet

#### 서블릿이란
자바 웹 어플리케이션 : html css 이미지 서블릿 jsp.. 이 구성으로 포함될 수 있다. 여러개 포함 될 수 있다. 

웹 어플리케이션은 WAS같은 미들웨어를 통해 실행한다 .
내가 전부 하는게 아니라 WAS를 통해 만든다면 그에 따른 규약을 따라야한다. 

그 약속중 하나인 <자바 웹 어플리케이션의 폴더 구조> ! 이 폴더 구조를 따라야한다. 
- xml 파일 : 배포 기술자. 웹어플리케이션의 관한 정보를 다 가진 파일이라 보면된다. 
 서블릿 3.0 미만은 xml파일이 필수, 3.0은 어노테이션이 역할을 대신한다. 

- classes 폴더에 서블릿 파일이 위치.


- 서블릿이란 : 자바 웹 어플리케이션의 구성요소 중 동적처리를 하는 프로그램의 역할 

- 서블릿은  WAS에서 동작하는 java 클래스이다. 
- 서블릿은 HttpServlet 클래스를 상속 받아야한다.
- 서블릿과 JSP로부터 최상의 결과를 얻으려면 웹 페이지를 개발할 때 jsp , 서블릿 두가지를 조화롭게 사용해야 한다. 


#### Servlet 작성 방법

방법 1) servlet 3.0 이상에서 사용하는 방법 
- 자바 어노테이션을 사용한다. 

방법 2) servlet 3.0 이하에서 사용하는 방법
- 서블릿 등록시 xml파일에 직접 등록한다. 

실습1 - 방법1 
새 프젝 생성할 때 다이나믹프젝버전을 눈여겨보자. 
마지막에 xml

요청이 들어왔을 때 이 서블릿이 실행되면서 응답할 코드를 만들어내고 , 만들어 낸 코드로 응답을 하는 것이다 -> 동적 페이지 

서버는 요청을 받아내는 객체와 응답을 하는 객체를 만들어낸다. 
response 객체에서 받을 객체가 무슨 타입인지 알아야 하기때문에 .setContentType()씀. 
--> 응답 보낼 내용 & 보내는 응답의 타입 
그 다음 무슨 내용으로 보낼 것이냐. 출력 메서드 객체 어쩌구 써서 한다...
tip) html 은 br을 넣어야 엔터가 되기때문에 print()를 쓰든 println()을 쓰든 상관없다. 

+) 자바 어노테이션이란??


실습2 - 방법2
-과정-
 
url /Ten 이라고 요청 들어와서 있으면 xml에서 servlet-name 을 확인하고 
<servlet>부분에서 display-name과 맞는 애를 찾고 servlet-class , 내가 실행 할 애가 누구인지 확인하는 것이다. 

url 바꾸고 싶으면 xml파일 url-pattern 부분을 바꾸면 된다. 


#### 서블릿의 생명주기
system.out은 콘솔에 보내는 것.  
print.out은 다른데다 보내느 것. 

요청이 객체가 메모리에 있나 없나? 
있으면 서비스만 호출된다. 
없으면 LifecycleServlet 객체 생성하고  init()생성하고 서비스 호출 
destroy 는 WAS가 종료되거나 웹 앱이 갱신 될 경우 호출된다. 

doPost ,, doGet ,,
 
<Requset, Response>
- HttpServletRequest 객체
- HttpServletResponse 객체

---
## less compile 하기

노드.. 
걸프 -미들도구 를 이용해서 

## transition을 이용한 css 기본 애니메이션
트랜지션  : 박스 엘리먼트가 움직일 속도를 조정해서 애니메이션 효과를 준다. css에 속성으로 선언한다.  구글링해서 참고하면서 작성해보잣 

### transform 속성 활용
transform : 이 속성을 이용해서 다른 엘리먼트에 영향을 미치지 않고 특정 엘리먼트의 위치를 바꿀 수 있다. 
translate 속성 추가하면 빠른 속도로 렌더링이 되는듯?
대체로 translate3d속성을 많이 쓴다. 


*20180520*
## PJ01 하면서 정리
- head와 header 태그 차이 
head는 구조적으로.. 서문같은 거다 
나타나게 하는 그런게아니었다 

- 시맨틱 태그의 중요성 , html 구조의 중요성

-배치의 이해 중요하다..
 layout작업 = renderin 과정 = 배치 : 엘리먼트를 화면에 배치하는 작업.
 
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

---

*20180522*

## CH02. DB 연결 웹 애플리케이션 
### BE
JDBC > spring JDBC 이용 할 것임. 
jps - 서블릿으로 바껴서 동작. 서블릿과 동작 같음. 

### FE
javascript , DOM ajax

### JavaScript -FE
자바스크립트 : 동적으로 컨텐츠를 바꾸고 멸티미디어롤 다루고, 움직이는 이미지등 웹 페이지를 꾸며주도록 하는 프로그래밍 언어. 
동적으로 구현. 

[출처] MDN_ 자바스크립트란?
#### 자바스크립트 변수 - 연산자 - 타입

- 자바스크립트는 컴파일 단계가 없다. -> 자바스크립트의 타입은 실행단계에서 결정된다. 
- 브라우저마다 자바스크립트실행 엔진이 있다. 자바스크립 버전은 ECMAScript(ES) 버전의 따라 결정된다. 
- 브라우저는 하위버전 지원한다. 

#### 변수 : [var, let, const]
어떤 것을 사용하는 가에 따라 scope(=변수의 유효범위)가 달라진다. 

#### 연산 
- 비교 연산자
== -> '같다' 라는 연산할 때 쓰면 오류날때 많음. 타입을 암묵적으로 바꿔서 비교하기 때문에 
다른 언어 쓰던 사람들이 아는 것과 다르게 나온다.  
=== -> 타입까지 비교 하기 때문에 더 정확히 나옴.

_중요!) == 많이 안쓰고 자바스크립에선 === 을 많이 쓴다._
+) && 연산자 : 모든 값이 true인지 확인하지만 첫번째가 이미 false이면 확인할 필요가 없다. 

##### Type [undefined, null, boolean, number, string, object, function, array, Date, RegExp ..] 
- 자바스크립은 타입은 여러개 존재하는데 타입을 쓰는 것이 없다. 
- 변수의 타입은 실행타임에 결정된다. 타입이 나중에 결정되는 것이다. 
- toString.call 통해서 자바스크립타입을 확인 할 수 있다. 

#### javascript 변수 / 타입 (출처 : MDN)
var : 동적타입 
기본 타입 
- Boolean 타입 : [true || false]
- Null 타입 : [null]
- Undefiend 타입 : 값을 할당하지 않은 변수는 undefiend 값을 가진다. 
- Number 타입 : 정수만을 표현하기 위한 특별한 자료형은 없다. 
                +, - 을 이용해 숫자 표현 할 수 있다. (ex. -1 +1 ..)
- String 타입 : 문자열의 자료형화를 조심하자. 문자열은 텍스트 데이터에만 사용하자.
                c 언어와는 다르게, 자바스크립트의 문자열은 변경 불가능하다. 하지만 원래 문자열에서 각각의 글자를 추출하거나 부분 문자열을 만들수 있다. 
- symbol 타입 : 유일하고 변경불가능한 기본값. 

tip:  배열의 경우 'forEach' 같은 메서드를 사용 하면 괜춘 / 가독성을 높히자

문자열 처리 
- 자바스크립은 문자 문자열 모두 문자열이다. 
- 문자열에 다양한 메서드가 있다. (.trim, .split, .relpace 등등 )

*20180523*

#### 함수 
- 함수 선언 / 함수 표현식
 : 파라미터의 개수와 인자 개수 일치안해도 오류가 나지 않고, 
 입력값 수가 파라미터 개수보다 작으면 그냥 'undefined'라는 값을 갖게된다. 
 초기화 됐지만 , 값이 할당되지 않았기 때문이다.  
 
** 호이스팅 : 함수 표현식으로 작성 할 때 관련. 
실행 될 때 한 줄 씩 실행 하는 것이 아닌 파서가 코드를 한번 쫙 훑는다. 
그래서 아랫줄에 선언 돼있어도 위로 끌어 올려서 쓰는 것처럼 해서 인식해서 처리하는 것. 
 
- 반환값 설정 안하면 'undefined'로 반환된다. 자바스크립트엔 void 타입이 없다.

tip) 함수표현식과 함수 선언문 두 가지 스타일이 있는데 하나만 정해서 쓰자. 

- arguments 객체 
함수 실행 되면 arguments (지역변수, 타입 : 객체) 자동생성. 
자바스크립트 함수는 선언한 파라미터보다 더 많은 인자를 보낼 수 있는데 , 이 때 넘어온 인자들을 
arguments로 배열의 형태로 하나씩 접근 할 수 있다. (하지만 배열타입은 아니기때문에 배열 메서드는 사용 불가능.)

+) arrow funcition 표현식 

함수 호출 스택 call stack : 함수는 연속적으로 불려질 수 있다. 이를 처리 하는 방법
- 메모리 모자르게 많이 쌓이면 오류난다. 

*180524* 
### WEB UI 개발 - FE

#### window 객체 (전역 객체) - setTimeout 메서드 
- 인자로 함수를 받고 있다.
- 콜백 함수다. 
- 비동기 함수이다. 
-> 콜 스택에 쌓여 있는 함수들 먼저 다 실행 된 후 (동기적인 실행 이 다 실행 된 후), 비동기가 마지막에 실행된다. 

> setTimeout ( function() {
>    실행할 것.
> }, 몇 초 )  

+) setInterval 

---

*180526*

#### DOM (Document Object Model)
- API
- 브라우저는 html 코드를 dom 이라는 객체 형태 모델로 저장한다.
- dom 루트 노드 : Document

document(루트 노드)의 DOM API (함수들)을 쓸 수 있다.
> .getEliementById("")
> .querySelector("dffdadff") ->  dffdadff 아이디 값 찾기
> .querySelector("#dffdadff") -> 태그가 dffdadff인 element 찾기
> .querySelector("(부모) .dffdadff") -> 부모 아래 dffdadff인 element 찾기
> (바로 아래 자식 찾는 거면 . 대신 -> 이거써도 ok )
> querySelectorAll : div인거 모두 찾기.

---

#### Browser Event / Event object, Event handler

##### Event
.addEventListener 함수 

객체.addEventListener("어떤이벤트(이벤트 이름)", function((매개변수)){
     //do something..
}, false);

: 어떤이벤트가 발생하면 함수가 실행되는데 , 이 함수가 이벤트 핸들러 또는 이벤트리스너

[참고 자료]
[link] (https://developer.mozilla.org/en-US/docs/Web/Events)
Introduction to events: [link](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#Event_handler_properties)

---

#### Ajax(XMLHttpRequest) 통신의 이해 - 비동기!

비동기로 서버로부터 데이터를 가져오는 것
요즘은 화면의 새로고침 없이, 화면의 일부분만 갱신 할 수 있다.

- JSON :  Ajax 를 위한 데이터 포맷 중 하나.

> XMLHttpRequest : 객체 생성.
> .open 메서드 : 요청 준비.
> .send 메서드 : 서버로 보냄.
> GET 방식으로 url 보낸다.

- setTimeout함수의 콜백함수의 실행과 유사하게 동작하는 '비동기' 로직이다.
-
+) CORS (Cross-Origin Resouce Sharing): Http 접근 제어
HTTP gpejemf


참고 자료 :
Ajax사용 예제 :[link]{https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#Event_handler_properties}

*180528*

### 자바스크립트 디버깅

## JSP
JSP의 이클립스 위치는 >webContent
모든 JSP는 서블릿!으로 바뀌어 서블릿으로 동작하고 java로 작성된다.
```
[문서 구조]
-지시문
-html
  - jsp
-html
.
.
```
```
 스크립틀릿 : <% %> 안에 있는 자바 코드.
<% 이 부분은 서블릿으로 바꿀때 어떻게 바껴야 하는지 알려주는 부분 %>

@ : 지시자.

<%= 브라우저에 응답결과로 넣고 싶은 부분 %>

out.print(랄랄라) --> <%= 랄랄라 %> 라고 생각 하면된다.

<%! jspService() 밖에 있는 필드나 메소드에 뭔가를 작성하고 싶다 할때 여기에 적는다. %>


```
---
#### 라이프 사이클
라이프사이클은 서블릿과 같다.

init() : 없으면 최초 생성. 
service() : 생성 된 후 호출 일 때 쓰인다.
destroy() : 수정 , 삭제 등 갱신 후 호출 할 때 destroy() 한 번 실행 후 init() 생성한다.

JSP 사이클 (실행순서)
1. 브라우저가 웹서버에 JSP정보를 요청.
2. 요청한 JSP가 최초 요청 일 경우 JSP로 작성된 코드를 서블릿으로 변환. (java 파일 생성)
3. 서블릿 코드 컴파일 --> 시행가능 bytecode로 변환 = class 파일 생성
4. 서블릿 클랫스 로딩하고 인스턴스 생성.
5. 서블릿이 실행 --> 요청 처리 앤드 응답 정보 생성.
---

---
#### JSP 문법

[요소]
- 선언문 <%! %> : 전역변수 선언 앤드 메소드 선언. JSP페이지 내에서 필요한 멤버변수나 메소드가 필요햘 때 선언한다. 
- 스크립트릿 <% %> : 프로그래밍 코드 기술. 지역변수 선언 됨
- 표현식 <%= %> : 응답 결과를 포함할 부분을 서술
- JSP페이지에서 사용할 수 있는 주석 : 
HTML 주석 : <!--랄라--> , jsp주석 : <%--랄라--%> , java 주석
하지만 상황에 따라 주석이 적용 되는게 달라지니 유의해서 사용하자. 
ex) 스크립트릿 내에는 자바쓰니까 자바주석.. 

---

---
#### JSP 내장객체
내장 객체 : 미리 선언하지 않아도 사용할 수 있게 미리 선언된 변수.
JSP 내장 객체 : JSP 실행하면 서블릿으로 바뀌어 작동한다. 서블릿소스 생성되고 실행된다. JSP에 입력한 코드들은 대부분 jspService()메소드 안에 
삽입 되는 코드로 생성되는데, 이 메소드에 삽입된 코드 윗부분에 미리 선언된 객체가 내장 객체이다. 

스크립트릿에서 자바 코드를 쓰는데, 자바를 쓰지만 자바와 다르게 내장 객체를 이용해 선언 안하고 바로 쓸 수 있다.  

---
*180530*

### redirect & forward - BE

#### redirect
: 서버 --> 클라이언트에게 어떤 url로 이동하라는 요청을 보내는 것. 
리다이렉트는 HTTP프로토콜 규칙이다. 
응답 상태코드: 302와 이동 할 URL정보를 Location헤더에 담아 전송한다. 
브라우저가 알아서 요청하고 받는다. 
~ ! 요청 객체 / 응답 객체가 2번 생긴다는 것을 기억하자 ! ~
서블릿 || JSP는 redirect 하기 위해 HttpServletResopnse가 가지고 있는 sendRedirect()메소드를 사용한다.

#### forword 
클라이언트가 서버에게 요청을 보낸다. 
서버가 요청을 받는 일을 서블릿이라한다. 서블릿 혼자 다 하진 않고 다른 서블릿에 처리한다. 
마저 다 처리한다음에 응답을 넘겨주는 것이 forward

!!리다이렉트와 포워드 차이 !!
클라이언트가 서버에게 요청 보내면 
-redirect
클라이언트가 서버에게 
서버가 클라이언트에게 다시 여기로 요청하세요~ 

-forward
클라이언트가 서버에게 요청을 보냈는데 
서버가 다른 누구(back)한테 해서 처리되는.. 클라이언트는 누구한테 보내고 뭐하고 이걸 알 필요가 없다 .
*forward는 요청이 '한 번'만 redirect는 요청이 '두 번'!!*
URL이 바뀌지 않는다.

#### servlet & JSP 연동
서블릿  <->  JSP : 상호보완적 관계
  |           |
 로직        HTML
  |___________|
     forward

- 서블릿에서 얻은 값을 JSP에서 쓰고 싶을 때 request.setAttribute("맡길 이름")를 이용하자. 
- forward 할 때 쓰는 request.getRequestDispatcher(요청 할 거 (jsp나 servlet))
  디렉토리 아래에 저장한 곳이면 디렉토리 써줘야 한다.

- 맡겨둔 것을 받을 땐 request.getAttribute

+) JSP에서는 자바코드를 줄이는 것이 좋다 그래서 나온 것이 --> EL표기법  , JSTL .. 

+) 하나의 서블릿에서 여러 개의 요청을 받는 방법 : 서블릿 URL mapping에서 와일드카드 ('*'기호) 사용해서..
[참고] : [link]{http://docs.roguewave.com/hydraexpress/3.5.0/html/rwsfservletug/4-3.html}


### scope - BE
변수 범위 설정에 관한 것.
JSP는 applicatino, session , reques, PageContext 내장 객체가 있다. 
값 저장 할 땐 .setAttribute() 불러올 땐 .getAttribute() 쓴다.  

#### 4가지 scope

1) Application : 하나의 어플리케이션 생성 - 소멸 까지 쓰일 수 있음.
웹 어플리케이션 하나당 하나의 application 객체 사용. 
! 모든 클라이언트가 공통으로 사용해야 할 값들이 있을 때 사용해야한다
하나의 웹 어플리케이션 안에 jsp나 서블릿등이 서로 공유할 공통 값

2) Session : session 객체가 생성돼서 소멸 될 때까지 . 요청이 여러개 들어와도 남아있다. 상태유지 할 때 쓰인다.
웹 브라우저 별로 변수 관리 할 때 쓴다. 각 브라우저는 하나의 클라이언트. 하나의 클라이언트마다 관리하는 객체. 
웹 브라우저간의 탭간의 세션 정보는 연동된다. 


3) request : 클라이언트 요청이 와서 서버가 응답을 보낼 때까지 사용 할 수 있는 scope.
forward할 때 reuqest 는 같고 서블릿1 서블릿2는 서로 페이지 스코프가 다르다.
-포워드 되는 동안 유지하고 싶은 정보가 있을 때 쓴다.
HttpSErvletRequest객체 사용.


4) page : 페이지 안 에서만. 하나의 특정 서블릿이나 JSP 가 실행 되는 동안에만 정보 유지. 
- PageContext (: 내장 객체) .setAttribute || .getAttribute
forward (ex. 서블릿1이 서블릿2로 넘어가면) 페이지 스코프가 달라진다. 
- 마치 지역변수로 사용 된다는 것이 다른 scope들과 다르다.

*180604*

## EL (Expression Language) : 표현 언어
값을 표현하는 스크립트 언어 . JSP의 기본 문법 보완 역할.
디자이너가 보기에 잘 표현 할 수 없을까? 의문에서 발전했다.
장점 : 자바를 사용 하는 것보다 깔끔하게 표현 할 수 있다.

- 문법
${랄라라}
${<표현1>.<표현2>}
주의! 비교연산자 > , < .. 꺽쇠는 html이랑 혼동 할 수 있으니 영자로 쓰자.

+) 표현언어 (EL) 비활성화 하기 - JSP에 명시하기 : <%@ page isEXIgnored = "true"%>
- EL에서 사용 할 수 있는 기본 객체

*180607*

## JSTL (JSP Standard Tag Library)
프론트 개발자가 보기 쉽게 하여 유지 보수 쉽게한다. -> 자바랑 섞여 있는 문서를 html tag
형태로 통일 한다.
html tag 형식으로 조건문 처리, 반복문 처리 변수선언 등 할 수 있다.
prefix tag 내가 바꿀 수 있다.

객체의 프로퍼티 - getter setter를 생각 하면 된다. (약속을 꼭 지켜서 작성하자)

forEach - 배열이나 리스트에서 저장된 요소를 뽑아 낼 수 있다. 


url 연결태그 -import 
param .. 부분에 연결할 url 값 넣어준다 .


*180608*

## SQL 
사람 <-> DBMS 간의 명령. 
DML / DDL / DCL 

<쿼리문 tip>
 .* : 모든 권한을 주겠다 
 @'%' : 어떤 클라이언트에서든 접근 가능.
 @'localhost' : 해당 컴퓨터에서만 가능. 
 
 
 
권한 부여 쿼리 후 flush privileges; 명령 꼭 하기. (db 반영)

[desc 테이블명] 또는 [describe 테이블명] 명령

.
.
.

*180609*
## Maven

+) pom.xml 파일 작성방법 조사하기

## JDBC
방법 앤드 절차 규약. 자바를 이용해 db접속 , 쿼리 실행 그리고 결과로 얻은 데이터의 핸들링을 제공한다.

[JDBC 이용한 프밍 방법]
1단계 : import java.sql.*;
2단계 : 드라이버를 로드한다. -> 각각DB 벤더를 연결한다. 
3단계 : Connection 객체를 생성한다 -> DB접속 절차
4단계 : Statement 객체 생성 및 질의 수행 -> 쿼리문 생성 실행을 Statement 객체가 도와준다 .
5단계 : SQL 문에 결과물이 있다면 ResultSet 객체를 생성한다. -> 쿼리문이 무엇이냐에 따라 다를 수 있다. (select는 조회하는 거고 insert는 한 후 잘 됐다 ~
이런 결과를 주는 차이에서 차이..)
6단계 : 단계 다하고 꼭 모든 객체를 닫는다. (생성관계 반대 순서로 닫는다. )
JDBC 클래스 생성 관계 : DriverManager -> Connection -> Statemnet -> ResultSet 


JDBC 실습
tip. 메이븐 설정하고 꼭 메이븐 업데이트해주자 .
+) 카멜표기법 지키기.

*180610*

## Rest API
Rest API란? 다양해진 클라이언트 종류에 정보 제공하는 방식을 일원화 시키는 방식 중
HTTP 프로토콜로 API를 제공하는 대표적 방식.

REST 구성 : 자원 (URI) + 행위 (HTTP method) + 표현

[출처] edwith, http://meetup.toast.com/posts/92


## webAPI 실습
- /~~~/* : 별표 의미 : 무슨 문자든 올 수 있다. 


JS : DOM / Event / Ajax
특히 자바스크립트 함수 이해.

*180617*

## PJ02 DB 연결한 웹어플리케이션 : TO-DO List 

- html로 웹 UI 구조 잡기. 
- 구조 잡은 html css로 꾸미기.
- window 객체 _ .setTimeout과 비동기 
동기적인 다른 실행이 끝난 후 실행된다.

- DOM 
브라우저는 elemnet를 DOM Tree형태로 저장한다. 
자바스크립트로 구현해서 html element를 찾기엔 복잡하다. 
DOM API를 이용하여 쉽게 html element를 찾을 수 있다. 

1. getElemnetById() : ID 정보를 통해서 찾을 수 있다. 
2. Element.querySelector() : 
+) Element.quierySelectorAll()
3. css selector

- 이벤트 리스너 

- AJAX(XMLHttpRequest 통신) : 비동기 통신




*180715*
### 자바스크립트 배열
#### 배열의 유용한 메서드들
- .indexOf()
문자열 있나 확인도 됨
결과는 -1보다 큰지 작은지로 판단.

- .join()
- .concat() : 원래 배열은 그대로 있고 합쳐진 새로운 배열을 반환한다.
- .join
- .slice

...

원래 배열을 반환할 수도 있고 새로운 배열을 만들 수도 있다.
원래 배열이 변경 될 수 있으니 조심하자.

*오늘 중요한 3대장 함수*
- forEach() : 함수를 매개 변수로 받을 수 있는 for문
- map() : forEach처럼 함수를 매개변수로 받는 함수. 새로운 배열을 반환한다.
- filter()

+) reduce / some / every ...

*반환값이 중요하다. 새로운 배열을 반환하는지 기존의 배열을 반환하는지*

### 자바스크립트 객체

자바스크립트 객체 : (key + value) 로 이루어진 'dictionary 자료구조'

배열 : 순서가 있는 리스트.
객체 :  키값을 이용한 자료구조.

[객체 탐색]
/* var obj = {key : value} */
obj.key || obj.["key"]


- for-in 문 -> 객체값 찾는데 많이 쓴다.
- object.keys 랑 forEach 이용해서 하는 방법도 있다.

### DOM API
#### DOM node 생성 & 추가

- firstChild : 공백까지 노드로 인식한다.
- firstElementchild : 이걸 이용하자 --...

#### 문자열기반으로 DOM 조작하기

tip : 크롬 개발도구 elemnet 클릭 후 콘솔창에 $0쓰면 클릭한 element가리킴.

- 노드 . closest("section") : 이 노드의 섹션 태그를 찾아준다. 이러면 계속 parentnode 쓸 필요 없다.

### ajax + 크롬개발자도구로 디버깅 보기
responseText로 온 문자열은 브라우저에 표시하기 위해서 jsonParse를 이용해 객체화 시켜 출력되게 한다.

+) 동영상보고 비동기 통신 과정 정리해보긔
+) JSONP

*tip : 크롬개발자 도구에서 녹화기능은 반응속도를 체크할 때 좋다. *

### 웹 애니메이션의 이해

간단한 방식은 css3의 transform과 transition 속성을 이용하는 것이다.

- FPS : 1초에 화면에 표현 할 수 있는 정지화면(frame) 수.  16밀리세컨드 간격이 적당하다. (1000/16)

간단하고 규칙적인 것 ->css로.
세밀한 조정 -> 추가로 자바스크립 이용.

- setInterval (이거 가지고 애니메이션 구현은 잘 안함)
: 내가 준 시간에 따라 실행.
단점 -> 이벤트 콜백이 지연되어 지연문제가 발생 할 수 있다.

- setTimeout
재귀적으로 호출한다. 끝난 다음에 또 부르고 끝난 다음에 또 부르고....
끝난 다음에 실행 되는 것이기 때문에 먹히는 거 없이 (?)  할 수 있지만, 지연문제를 간과 할 순 없다.
timeout을 조절해 컨트롤 할 수 있다는 것이 setInterval과 다르다.


그렇다면 이거 말고 많이 사용하는 것은 ?
#### requestAnimationFrame

#### requestAnimationFrame활용
- 애니메이션을 위한 전용 함수.
- 함수 탈출 조건으로 컨트롤. 
- 16 밀리세컨드 이하 간격으론 권장하지 않는다. 

#### CSS3 transition 활용 
모든 css속성을 애니메이션과 함께 1초동안 변화 시키자. 
css / transition / transform .. 이 빠르다. 

+) vendor prefix


*180726*
#### QnA day

- 상대적 링크 : local8080.. 이거 말고->  ./ 으로 사용하자. 배포시 사용자의 port가 사용자마다 다를 수 있기 때문이다. 
- click.js 의 todo || doing if문 리팩토링
- main문 css 가운데로 하기 

- HTML5형식으로 작성하길 권장 -> 그럼 DOCTYPE 선언 안 해도됨.

- '지킬' 이용해서 깃헙에 정적 블로그 만들기

면접 때 ex: sping으로 Vue 나.. 이런거 이용하지 않고  순수 자바스크립트로 뭘 만들어 봤다.
이런거 배웠고 앞으로는 이런 걸 응용해서 어떤 걸 만들고 싶다
일일 커밋 매일하기. 부코 강의에 나오는 코드는 깃헙에 올려도 괜춘 !

마루180
아산나눔재단 


*180728*
### DOMContentLoaded
- DOM ContentLoaded : DOM Tree를 먼저 모두 로드 됐을 때를 알린다. (document)
- Load :모든 이벤트들 .. 모두 로드 했을 때 . (window)

보통 html, css... 등 브라우저 렌더링 작업이 모두 끝난 후 이벤트 실행, 노드변경 찾는 등의 JS는 html 맨 아래 쪽에 위치 시킨다. 
하지만 이렇게 해도 DOMTree가 전부 구성 되기 전에 JS 실행 되는 경우가 있다.
DOMContentLoaded 이벤트는 DOM Tree가 모두 로드 되어 구성됐을 때를 알린다.
때문에 DOMContentLoaded 이벤트 안에 DOM Tree 모두 로드 후 실행 시킬 일들을 써주면 좋다. (노드 찾기 , 구성등..)

### Event delegation (기법) : 부모 엘리먼트에 위임한다.
list가 각자 UI에 각각 비슷한 이벤트를 걸어 처리해야 한다면 어떻게 해야할까 ?  
이벤트 등록을 효율적으로 어떻게 할까 ? for문을 쓸까?

맨 상위 엘리먼트에 이벤트 리스너 등록하면 하위 엘리먼트 클릭해도 된다!

+) firstChild / firstElementChild 차이
firstElementchild 공백 확인

브라우저가 기억해야 할 이벤트 핸들러가 많이지면 메모리사용이 비효율적으로 된다.

그럼 어떻게 ? -> target정보를 이용하자
target : 내가 클릭한 지점 정보.

- Bubbling : 하위 엘리먼트를 클릭 했더라도 상위 엘리먼트 쭉쭉 검색 올라가면서 그 중에 등록한 이벤트 리스너가 있다면 실행된다.
기본적으로 버블링 순서로 이벤트가 발생된다.

- Capturing : 버블링과 반대로 이벤트 발생.
캡처링으로 이벤트 발생 시키고 싶다면 addEventListener 메서드 3번째 인자값을 true 지정.

[발생 순서] 
ex) Element 1 > Element 2 > Element 3 이라면,  
캡처링 : 1 -> 2 -> 3 / 버블링 : 3 -> 2-> 1

<예제 코드>
ul.addEventListener("click", function(evt){
   // target이 image이면 src를 추출해서 출력한다.
   var target = evt.target;
   if(target.tagName === "IMG") {
      log.innerHTML = "IMG URL은, " + target.src;
   }

})

만약 이미지들 사이 패딩을 클릭해도 이미지 정보가 나오게 하고 싶다면 ,

<예제 코드>
ul.addEventListener("click", function(evt){
   // target이 image이면 src를 추출해서 출력한다.
   var target = evt.target;
   if(target.tagName === "IMG") {
      log.innerHTML = "IMG URL은, " + target.src;
   } else if (target.tagName === "LI") {
      log.innerHTML = "IMG URL은," + target.firstElementChild.src;
   }

})


#### HTML templating 작업
서버로부터 받은 데이터를 화면에 반영해야 할 때가 많은데, 
HTML 형태는 그대로인데 데이터만 변경되는 경우는 어떻게 처리해야 효율적일까?

- HTML templation :  HTML과 데이터를 섞어서 표현하는 방법.

보통 백엔드에서 데이터 조회 후, 그 내용들을 동적으로 HTML로 만들어 클라이언트에 보내준다.
회사에서도 동적으로 클라이언트에서 생성할까 서버에서 할까 고민이다..

서버에서 보내준 JSON Data을  HTML Template 에 알맞게 넣어주면 이것이 HTML templating !

- String의 replace
.replace() 메서드를 쓴다.

+) regular expression 을 쓰면 더 막강해진다.

repalce는 메서드 체이닝 방식으로 호출하면서 풀이 할 수 있다.
*메서드 체이닝*

data가 배열 형태로 여러개면 간단한 반복문 또는 forEach같은 메서드 사용.

<예제 코드>
var data = {
              title: "hello",
              content : "chicken"
              price : 20000
           };
           
var html =
"<li>
<h4>{title}</h4>
<p>{content}</p>
<div>{price}</div>
</li>";

html.replace("{title}", data.title)
    .replace("{content}", data.content)
    .replace("{price}", data.price);



어떻게 템플릿을 보관 할 수 있을까?

JS를 정적 데이터로 html로 넣는 건 좋지않다. 다음 두가지 방법이 있다.

1) 서버에 file로 보관헤서 Ajax로 요청 받아온다.
2) HTML 코드 안에 숨겨둔다

HTML script태그는 type이 javascript가 아닌건 렌더링 안하고 무시한다. 이 속성을 이용해 type은 내맘대로 쓰고 HTML Template을 숨겨둔다.!
추가로 ES6에의 템플릿 리터럴이라는건 repalce를 안쓰고 편하게 된다.

<예제 코드>

<script id="template-list-item" type="text/template">
 <li>
  ~~~~~내용~~~
 </li>
</script>

<script>
  //위에 선언한 JS의 id값을 DOM Api를 이용해 가져올 수 있다.
  //.innerHTML DOM Api를 이용해 데이터를 뽑아오자.
   var html = document.querySelector("#template-list-item").innerHTML
</script>

var data = [
        {title : "hello",content : "lorem dkfief",price : 2000},
        {title : "hello",content : "lorem dkfief",price : 2000}
];

var html = document.querySelector("#template-list-item").innerHTML;

var resultHTML = "";

for(var i =0; i< data.length; i++){
   resultHTML += html.replace("{title}", data[i].title)
                     .replace("{content}", data[i].content)
                     .replace("{price}", data[i].price);
}

document.querySelector(".content").innerHTML = resultHTML;


+) innerHTML말고 특정 부위에 넣고싶을 때 쓰는 메서드는 insertAdjacentHtml 이나 insertBefore....


#### Tab UI를 만들기 위한 HTML과 CSS 구조전략

- Tab UI Component

+) tap UI 클릭시 ajax로 데이터를 받아올 때, 매번 똑같은 데이터를 새로 받아오지말고
이미 가져온 데이터는 배열로 저장하고 재사용 하도록 하자 -> 캐쉬 기능


*180720*

### Spring (프레임워크)

프레임워크 : 반제품 
모듈화가 잘돼있다. 전부 다 알 필요 없고, 필요할 때 필요한 것을 사용하자.
+) AOP

[스프링 웹 계층]
- spring-web 모듈 : 멀티파트 파일 업로드  / 서블릿 리스너 등/// 
- spring-webmvc 모듈 : 다른 말로 Web-servlet모듈. Spring MVC 및 REST 웹 서비스 구현 .
- spring-websocket 모듈
- spring-webmvc-portlet 모듈


[스프링 프레임워크 핵심 개념]
- Container
- IoC (Inversion of Control)
- DI (Dependency Injection )


- Container
인스턴스 생명주기 관리. 인스턴스의 생성 부터 소멸까지 내가 직접하는 것이 아니라 컨테이너가 알아서 해준다. 
앞 시간에서 배웠듯이 Tomcat이라는 WAS가 가지고 있는 컨테이너가 servlet 생성 ~ 소멸 관리한다.  JSP 

- IoC (제어의 역전)
inversion : 도치, 역전 

예를 들어 , 일상에 있는 tv 리모컨의 기본적인 구성과 기능 인터페이스가 동일 한 것과 
TV공장을 만든다. -> 이 부분을 spring이 대신 해준다. 
                   스프링이 가진 공장 2개 : 1) BeanFactory: 완전 간단기능만 있음. 
                                        : 2) ApplicationContext : 빈팩토리 +a 그래서 더 많이 쓰인다.

어노테이션.. 

- DI (의존성 주입)
컨테이너가 생성한 객체를 받아 온다. 
그렇게 공장에서 만들어진 인스턴스를 가져올 수 있는 방법 중 하나이다.


*180729-31*

#### Spring MVC
- MVC :
Model : 뷰가 렌더링하는데 필요한 데이터. 예) 상품목록..
View : 웹 어플에선 실제로 보여지는 부분. JSP ,XmL등으로 표현한다.
Controller : 사용자의 액션에 응답하는 컴포넌트. 모델 업뎃, 다른 액션을 수행.

- MVC MOdel 1 아키테처

(그림)

java bean 을 이용해서 db를 이용 . JDBC의 Role Dao 와 유사
문제점 : jsp 에 java , html이 섞여 있어서 유지 보수 힘듬

- MBC Model 2 아키텍처

(그림)

요청 자체를 서블릿이 받게 하고/.. 아래 와 같이 나눠서 구현
컨트롤러 - 서블릿
뷰 - jsp
모델 - 자바 빈

- MVC Model 2 발전형태
프론트 컨트롤러 : 서블릿이 수행하고 딱 하나만 존재한다. 요청만 받고 컨트롤러(핸들러)에게
일을 위임 .
컨트롤러는 java bean과 같이 .. 수행 한다음 담아서 프론트 컨트롤러에 보냄

=> 이런  model 2 패턴을 모듈 지원하는게 Spring MVC !!!!

#### Spring MVC 구성요소 *순서 이해 필수 !!*

[Spring이 제공하는 부분들]

- DispacherServlet (= 프론트 컨트롤러 = 전화교환부서와 같은 역할?)
디스패처서블릿에 사용되는 컴포넌트 (객체)에는 어떤 것들이 있을까
모든 요청을 여기서 받는다. 요청을 처리할 컴포넌트와 메서드를 핸들러 매핑에게 물어본다.
요청 받아서 넘겨주는 일 '만' 한다.
보통은 한 개 만 선언한다.

<Dispatcher Servlet  내부 동작 흐름>
1. 요청 선처리 작업
- 디스패처서블릿는 지역화Locale(미국사람은 미국세팅 , 한국사람은 한국세팅)를 지원한다.
HTTP 헤더 정보 보고 지역을 결정한다.

- RequestContedxtHolder에 요청 저장 : httpServletrequest 어쩌고 .. 저장해서 막 쓰기? 근데 문제 가 될 수 있다.

- FlashMap 복원 : 현재 실행이 redirect 됐을  , url 복잡한 걸 복원..?

- 멀티파트요청  y/s : 멀티파트 파일 요청을 정하는 파트다.

- 요청 작업

[요청 선처리 작업시 사용된 컴포넌트] - 강의자료
1) org.springframework.web.servlet.LocaleResolver
- 지역 정보를 결정해주는 전략 오브젝트이다.
- 디폴트인 AcceptHeaderLocalResolver는 HTTP 헤더의 정보를 보고 지역정보를 설정해준다.

2) org.springframework.web.servlet.FlashMapManager
- FlashMap객체를 조회(retrieve) & 저장을 위한 인터페이스
- RedirectAttributes의 addFlashAttribute메소드를 이용해서 저장한다.
- 리다이렉트 후 조회를 하면 바로 정보는 삭제된다.

3) org.springframework.web.context.request.RequestContextHolder
- 일반 빈에서 HttpServletRequest, HttpServletResponse, HttpSession 등을 사용할 수 있도록 한다.
- 해당 객체를 일반 빈에서 사용하게 되면, Web에 종속적이 될 수 있다.

4) org.springframework.web.multipart.MultipartResolver
멀티파트 파일 업로드를 처리하는 전략

2. 요청 전달
HandlerExcecutionChain 발견했냐 안했나 판단-> 발견 못했으면 에러 400대
HandlerExcecutionChain 있으면 HandlerAdapter객체가 결정된다
만약 핸들러어댑터 없으면 서버 잘못 -> 서블릿예외 발생시킨다.
문제 없으면 요청 잘됨.

Handler Mapping  디폴트 설정들..

[요청 전달 시 사용된 컴포넌트]
1) org.springframework.web.servlet.HandlerMapping
- HandlerMapping구현체는 어떤 핸들러가 요청을 처리할지에 대한 정보를 알고 있다.
- 디폴트로 설정되는 있는 핸들러매핑은 BeanNameHandlerMapping과 DefaultAnnotationHandlerMapping 2가지가 설정되어 있다.

2) org.springframework.web.servlet.HandlerExecutionChain
- HandlerExecutionChain구현체는 실제로 호출된 핸들러에 대한 참조를 가지고 있다.
- 즉, 무엇이 실행되어야 될지 알고 있는 객체라고 말할 수 있으며, 핸들러 실행전과 실행후에 수행될 HandlerInterceptor도 참조하고 있다.

3) org.springframework.web.servlet.HandlerAdapter
- 실제 핸들러를 실행하는 역할을 담당한다.
- 핸들러 어댑터는 선택된 핸들러를 실행하는 방법과 응답을 ModelAndView로 변화하는 방법에 대해 알고 있다.
- 디폴트로 설정되어 있는 핸들러어댑터는 HttpRequestHandlerAdapter, SimpleControllerHandlerAdapter, AnnotationMethodHanlderAdapter 3가지이다.
- @RequestMapping과 @Controller 애노테이션을 통해 정의되는 컨트롤러의 경우 DefaultAnnotationHandlerMapping에 의해 핸들러가 결정되고,
그에 대응되는 AnnotationMethodHandlerAdapter에 의해 호출이 일어난다.

3. 요청 처리
익스큐선체인 결정되면 사용가능 인터셉터가 있는지 찾아본다
*인터셉터 : 필터 같은거
인터셉터 잇으면 실행 하고
핸들러 실행 후 리턴값 준

[요청 처리시 사용된 컴포넌트]
1) org.springframework.web.servle.ModelAndView
- ModelAndView는 Controller의 처리 결과를 보여줄 view와 view에서 사용할 값을 전달하는 클래스이다.
Request에다 값을 넣어서 사용하는 것보다 이 컴포넌트를 쓰는게 바람직.

- .RequestToViewNameTranslate
 컨트롤러에서 뷰 이름이나 뷰 오브젝 제공하지 않았을 떄 적절하게 제공 해주는 ..

 4. 예외처리

 [예외 처리시 사용된 컴포넌트]
1) org.springframework.web.servlet.handlerexceptionresolver
- 기본적으로 DispatcherServlet이 DefaultHandlerExceptionResolver를 등록한다.
- HandlerExceptionResolver는 예외가 던져졌을 때 어떤 핸들러를 실행할 것인지에 대한 정보를 제공한다.

5. 뷰 렌더링 과정
- View Resolver

[뷰 렌더링 과정시 사용된 컴포넌트]

1) org.springframework.web.servlet.ViewResolver
- 컨트롤러가 리턴한 뷰 이름을 참고해서 적절한 뷰 오브젝트를 찾아주는 로직을 가진 전략 오프젝트이다.
- 뷰의 종류에 따라 적절한 뷰 리졸버를 추가로 설정해줄 수 있다.

6. 요청 처리 종료


(정리하자면)
- Handler Mapping
어떤 요청에 어떤 컨트롤러가 동작할지 .xml이나 .java에 어노테이션으로 설정한 것을
핸들러 맵핑 객체들 생성되면서 관리하는 역할 .

- Handler Adapter
결정된 메서드앤 컨트롤러를 핸들러 어댑터에게 요청 앤드 실행 한 후 결과를
모델에 받아서 다시 디스패처서블릿에 준다.

- View Resolver
어떤 뷰다 라고 알려주면 뷰가 출력한다.


#### Spring MVC 실습

(실습 내용)
웹브라우저에게 url 요청 후  - > 2개 값 입력 받을 수 있는 창& 버튼 있는 화면 출력
-> 웹브라우저에 2개 값 입력 하고 버튼 클릭하면 어쩌구 URL로 입력값 post로 서버에게 보내고
-> 서버는 2개 값 더 해서 결과값 JSP에게 request scope로 전달해서 출력하긔

1. [pom.xml 설정 하기]
plugins : jdk 1.8
라이브러리 : jstl, jsp, servlet
spring-context
webmvc
버전 통일 위해 프로퍼티 추가

- DispatcherServlet이 FrontController이다 라고 설정하기

얘도 서블릿이기 때문에 web.xml 파일에 설정 할 수 있다.
두 가지 방법이 있다.
1) web.xml 파일에 dispatcherServlet 설정하는 방법
어떤 일을 할 지 알려주는 것...
java config sprin g설정 읽어 들이도록 . javaConfig 를 읽어온다.
urlpatten 에 맵핑할 url 넣으면 servlet-name 과 같은 name으로 매핑되어있는 servlet -class가 실행 된다 : 지난 강의 참조하기
슬러시를 쓰면 슬러시덕분에 모든 요청을 받을 수 있다.

2)  WebApplicationInitializer 를 이용해서 구현하기 : 수업에서 자세히 안다룸.
단점 : 첫 구동이 오래 걸릴 수 있다.

[쓰이는 어노테이션들]
- @Configuration
이 어노테이션을 통해 자바 config 파일이구나 알려주는 역할 이다.

- @EnableWebMvc
디스패처서블릿에서 필요한 애들 web에 필요한 빈들 자동 설정 해준다.
xml로 설정의 <mvc:annotation-driven/>와 동일한 애 -> 수업시간엔 안한다.

..버거월  ㅠㅠ 익숙해진 후 찾아보자

- @ComponentScan
Spring MVC에서 핸들러  = 컨틀로러 찾아야 하는데 componentScan 어노테이션 사용해서
내가 직접 만들었던 빈을 이용해 직접등록도 되고 ..
@ComponentScan (basePackages = {}) -> basePackages 꼭 설정해줘야 어디서부터 찾을 지 알 수 있다.

- @EnableWebMvc
설정 자동 로드 됨 . 수동 설정 하고 싶다면 다른거 있음
이거 안쓰면 webMvcContextConfit-support 상속 받아야함.

 - @Controller
이거 붙여야 컨트롤러인줄 안다. 맵핑 위해 @RequestMapping 서블릿 url지정시 @Servlet 관련 어노테이션
붙이는거랑 같다.

- addResourceHandlers

* 반드시 필요한 부분
registry.addResourceHandler("/css/**").addResourceLocations("/css/").setCachePeriod(31556926);
                      ----"/css/**"-------이렇게 들어오는 url요청은 ------"/css/----- 여기서 찾아요 라는 뜻임


registry.addViewController("/").setViewName("main");
// "/" 로 들어오는 애들은 main을 찾아줘요

리졸버  - 뷰 그릴수 있게 찾아주기 ?
어쩌구저쩌구 - ResourceViewResolver(){
   InternalResourceViewResolver resolver  = new Internal ResourceViewResolver();
   resolver.setPrefix("/WEB-INF/views/"); // .setViewName("main") "main" 앞에 "/WEB-INF/views/" (찾는 거 해당 경로) 붙이기
   resolver.setSuffix(".jsp")// .setViewName("main") "main" 뒤에 ".jsp" 붙d여서 찾을 수 있도록
}


- 디스패처를 프론트 컨트롤러라고 설정해주기
web.xml  열어서.. 20분 쯤 부터
/ 로 들어오면

init-param 부분에서 앞서 webMvcContextConfiguration파일로 설정 잡아준거 등록

어쩌구-ApplicationConfiguration 이건 beans공장


[Controller 작성 실습]

controller 클래스에 꼭 @Controller 어노테이션 붙혀주기
@GetMapping(path  = "/dfdf") : get 방식으로 들어 올때 쓰는 어노테이션 / @PostMapping(path  = "/dfdf") : post 방식으로 들어올때 쓰는 어노테이션 .

(다양한 Controller 메소드 인수 타입 / 어노테이션)

@PathVariable  : 패스에서 받은 변수명을 받기 위하 ㄴplace holder가 필요함.
주의할 점 : 넣어준 이름과 파라미터명 잘 매치 되게 해줘야 스프링이 잘 넣어준다.

modelMap. 쓰면 requestScope에 알아서 넣어준다. 스프링의 다양한 객체들을 이용해보자

+) EL 표기법은 2.3버전땐 필수가 아니었다. web 버전 3.1로 했는지 체크하기

@RquestMapping @GetMapping @PostMapping ..
매핑하는 다양한 방식이 있다.

@RequestParam 통해서 하나 하나 받는거 말고
@ModelAttribute 어노테이션 붙여서 한꺼번에 가방처럼 들고다니는 DTO 를 만들어준다.

스프링이 알아서 넣기 때문에 form에서 쓴 name과 dto에서 쓴 name이 반드시 같아야 한다.
private 로 선언했는데 스프링이 접근하기 때문에 게터세터를 써줘야한다.
+) toString 을 쓰면 이름표처럼 뭐가 있는지 한번에 출력되게 하면 편하다 .


Controller 실습 3번
@GetMapping("/goods/{id}") -> {id} : 이 부분이 Path Variable
= url 요청이 왔을때 {id} 라는 path Variable로 받겠다.


*180731*
#### 레이어드 아키텍처
url 은 다르지만 웹페이지 요소 , 구성이 겹치는 부분이 있다면
Controller에서 중복되는 부분을 처리하려면?

1. 별도의 객체로 분리한다. 2. 별도의 메소드로 분리한다.

서비스 객체는 업무와 관련된 객체 = 비지니스 객체

서비스 객체란 ?
비지니스 로직을 수항해는 메소드를 가지고 있는 객체
1개의 비지니스 로직 -> 1개의 트랜잭션 동작
서비스 객체마다 비지니스 메서드를 가지고 있다.
서비스 객체 는 맞게 비지니스 메서드를 여러개 교차 사용 한다.
하나의 비지니스 메서드는 트젝 단위로 처리.

트랜잭션이란?
하나의 논리적인 작업을 의미.
[트랜잭션 특징 4가지]
1. 원자성
전체가 성공하거나 / 전체가 실패하는 것 .
ex) '출금' 기능 안에 작업들을 각각 볼 수 없고 , 이 안의 작업들을 모두 완료 해야 한 개의 기능으로 보는 것.
+) rollback : 오류 났을 때 앞에 수행 된 작업들을 원래대로 모두 복원 시키는 것.
+) commit : n번 작업까지 모두 성공했을 때만 정보를 모두 반영하는 것. 작업 반.
롤백 하거나 커밋 하게 되면 하나의 트잭 처리가 됐다고 하는 것이당 .

2. 일관성
트랜잭션의 작업 처리 결과가 일관성 있게 유지 되는 것.

3. 독립성
둘 이상의 트젝이 동시에 진행 되고 있을 때 어느 하나의 트젝이라도
다른 트잭 연산에 끼어 들 수 없는 특성. 하나의 특정 트젝이 완료 될때까지
다른 트젝이 사용 할 수 없다.

4. 지속성
트젝이 성공적으로 완료 됐을 때 , 결과가 영구적으로 유지 되는 특성을 지속성이라한다.

-JDBC 프로그래밍에서 트랜잭션 처리 방법-
DB 연결 된 후 connection 객체의 setAutoCommit메서드를 false로 파라미터 지정하고
커밋 조건 만족 후 커밋 되도록 조건들을 작성 해준다.
true면 자동 커밋 된다.

-스프링에서 트젝 활용-
@EnableTransactionMAnagement 이 어노테이션을 쓴다.
특정 트잭매니저를 사용하려면
TransactionManagementConfigurer를 Java Config파일에서 구현하고 원하는 트젝 매니저를 리턴하도록 한다.
또는 , 특정 트젝 매니저 객체 생성 시, @Primary 어노테이션 지정.


왜 레이어드 아키텍처가 사용될까?

<각 레이어의 구성요소>

Presentatino Layer : 컨트롤러 객체 동작 : 보여지는 걸 구현하는 레이어. 지금 과정에선 web
Service Layer : 서비스 객체 동작
Repository Layer : DAO 객체

무슨 로직을 어디 레이어에 놓아야 하나 .. 앞으로 고민하게 될 것.

*설정의 분리하기 :
Spring 설정 파일을 프리젠테이션 레이어쪽과 나머지를 분리할 수 있습니다.

web.xml 파일에서 프리젠테이션 레이어에 대한 스프링 설정은 DispathcerServlet이 읽도록 하고, 그 외의 설정은 ContextLoaderListener를 통해서 읽도록 합니다.

DispatcherServlet을 경우에 따라서 2개 이상 설정할 수 있는데 이 경우에는 각각의 DispathcerServlet의 ApplicationContext가 각각 독립적이기 때문에 각각의 설정 파일에서 생성한 빈을 서로 사용할 수 없습니다.

위의 경우와 같이 동시에 필요한 빈은 ContextLoaderListener를 사용함으로써 공통으로 사용하게 할 수 있습니다.

ContextLoaderListener와 DispatcherServlet은 각각 ApplicationContext를 생성하는데, ContextLoaderListener가 생성하는 ApplicationContext가 root컨텍스트가 되고 DispatcherServlet이 생성한 인스턴스는 root컨텍스트를 부모로 하는 자식 컨텍스트가 됩니다.

참고로, 자식 컨텍스트들은 root컨텍스트의 설정 빈을 사용할 수 있습니다.

[실습]

pom.xml 설정시 dynamic web 3.1로 수정안된다 어쩌구
오류 수정 참고 url : http://lng1982.tistory.com/199

web.xml 설정 설명 - 강의 두번째 꺼 12:49

쿼리에 'limit' 은 어디 일정 부분을 가져오는 쿼리문(?)
Dao에는 @repository 라는 어노테이션을 붙여주자.

어떤 메서드 구현 하고 나서 바로 테스트를 해주는 것이 중요하다.
근데 사실 개발하는 곳에 main 메서드를 여러개 넣어서 막 하는 것은 좋지않다.
JUnit 같은 단위 테스를 할 수 있는 도구를 공부해서 이용해보자.

문자 한글이여서 insert 안 될 때
참조 : http://ezsnote.tistory.com/entry/mysql-%EB%AC%B8%EC%9E%90%EC%85%8B%EC%9D%B4-%EC%95%88%EB%A7%9E%EC%95%84%EC%84%9C-insert-%EC%95%88%EB%90%98%EB%8A%94-%EA%B2%BD%EC%9A%B0-UTF-8
방법 1) 테이블 생성시 character set utf8 해주자.
방법 2) 기존 테이블의 charset을 바꿔주자.
참조 : http://archmond.net/?p=7659

방법 3) mysql 설정 자체를 바꾸자.

서비스 인터페이스들만 가지고 있는 패키지 : service
실제 구현체 가지고 있는 패키지 : service.impl

+) java implements란?
+) 인터페이스란 


#### Restcontroller

Spring MVC를 이용해 Rest API작성하는 방법 .

Rest API / Web API / @RestController / MessageConvertor

@RestController
- Spring 4에서 Rest API 나 Web API를 개발하기 위해 등장한 어노테이션.
- 이전 버전의 @Controller랑 @ResponseBody 를 가지고 있다.

JSON 객체 받은 걸 해석해주거나 보낼때도 작성해서 보내는 역할을 한다...
jackson 을 쓰기 때문에 꼭 ! jackson 라이브러리를 추가해줘야 오류가 안난다.

MessageConvertor
- 자바 객체 & HTTP요청/응답 바디를 변환한다.
- @ResponseBody , @RequestBody
- @EnableWebMvc로 인한 기본 설정
- WebMvcConfigurationSupport를 사용해서 Spring MVC 구현
- Default MessageConvertor를 제공한다.
- 링크 바로가기 의 addDefaultHttpMessageConverters메소드 항목 참조

++++ Messageconvertor 종류 ++++++
ByteArrayHttpMessageConverter
StringHttpMessageConverter
ResourceHttpMessageConverter
SourceHttpMessageConverter
FormHttpMessageConverter
Jaxb2RootElementHttpMessageConverter
MappingJackson2HttpMessageConverter
MappingJacksonHttpMessageConverter
AtomFeedHttpMessageConverter
RssChannelHttpMessageConverter

JSON 응답하기
- Controller의 메소드에선 JSON으로 변환될 객체를 반환한다.
- jackson라이브러리를 추가하면 JSON으로 변환하는 MessageConvervor가 사용되도록
@EnableWebMvc에서 기본으로 설정되어 있다.
- jackson 라이브러리를 추가하지 않으면 JSON메세지로 변환할 수 없어서 500대 오류가 발생한다.
- 사용자가 임의로 Messageconverter를 사용하도록 하려면 WebMvcConfiguerAdapter의
confitereMessageConverters메서도를 오버라이딩 하도록 한다.


#### pj03 진행 하면서 이슈 
- 배포경로 -워크스페이스 경로 문제
context path : root 
웹 어플리케이션 경우 (이 실습 , 이클립스-톰캣 -maven webapp일 경우 ) context path 는 webapp 이다.
webapp
  - WEB-INF
      -jsp  <- 여기에 위치한  .jsp의 경로 작성 해야 할 경우: ./WEB-INF/jsp가 된다. 
 
./ : 상대 root 경로 

ex) ./서블url  ./jsp/main.jsp


function updateTransition() {
  var el = document.querySelector("div.box");
   
  if (el) {
    el.className = "box1";
  } else {
    el = document.querySelector("div.box1");
    el.className = "box";
  }
   
  return el;
}

var intervalID = window.setInterval(updateTransition, 7000);


### 오프라인 강의 - BE : spring을 spring boot 2.x 바꾸기


-JUnit 이용한 테스트 익히기.

### 오프라인 강의 - FE
- 주니어와 시니어의 차이 ?
1-2명을 이끌면서 유지보수까지 다 고려해서 요구사항을 만들 수 있냐
구체적으론 서비스 부분을 만들 수 있냐
javascript를 할 줄 알아야
FE로 가도 BE와 어떻게 통신되는지를 최소한 알아야 한다. 

MV* : 서로 객체 간의 느슨한 관계를 알아야 ... 객체 지향 프로그래밍 책이 도움이된다 (java)

FE는 다음 두가지를 잘하면 잘한다 할 수 있다. = 중요하다.
1) 템플릿 작업을 세련되게 한다.   2) 비동기를 잘 제어 할 수 있다. 

Rounting --> 히스토리 

MV* / js es5(우리나라 하위버전 있어서 포용 해야하기 때문) , es6(es2015)/ 비동기/ compoment design / routing
==> 결과적으로 js 의 이해가 중요하다. 

한 개를 다른 패턴으로 바꿔보면서 깊게 개발. 

백엔드는 잘 나눠져있는데(스프링..) , 프론트엔드는 프레임워크가 없으면 가이드라인이 없어서 모듈나누기가 힘듬.

### 오늘의 실습 : Fetch API를 이요해서 templating 작업하기.
promise 패턴으로 만든 것이 Fetch API.

hello => () 이거랑 function hello () 똑같은 것.

.then : 통신이 되면 실행 

#### PJ02 리뷰 + 공뷰
- final 상수와 상수명명법 
1) final 상수 이름지을 땐 대문자를 쓰고, 두가지 이상 뜻의 결합은 _ 표시를 이용해 표현한다.   
2) final 변수에 대한 이해 : 내부 로직상 변경 되면 안되는 상수에 final 키워드를 명시한다.  
final 변수로 선언하고, 변수가 변하게 코딩하여 컴파일하면 오류가 발생한다. 

ex) public static final int a;

