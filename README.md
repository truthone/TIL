
*180511*

## ch.1 html을 통한 웹사이트 구조 설계 

#### HTML 이란?
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

---

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


## 20180522

DB 연결 웹 애플리케이션 
[BE]
JDBC > spring JDBC 이용 할 것임. 
jps - 서블릿으로 바껴서 동작. 서블릿과 동작 같음. 

[FE]
javascript , DOM ajax

### JavaScript -FE
<자바스크립트 변수 - 연산자 - 타입>

- 자바스크립트는 컴파일 단계가 없다. -> 자바스크립트의 타입은 실행단계에서 결정된다. 
- 브라우저마다 자바스크립트실행 엔진이 있다. 자바스  립 버전은 ECMAScript(ES) 버전의 따라 결정된다. 
- 브라우저는 하위버전 지원한다. 

변수 : [var, let, const]
어떤 것을 사용하는 가에 따라 scope(=변수의 유효범위)가 달라진다. 

연산 
- 비교 연산자
== -> '같다' 라는 연산할 때 쓰면 오류날때 많음. 타입을 암묵적으로 바꿔서 비교하기 때문에 
다른 언어 쓰던 사람들이 아는 것과 다르게 나온다.  
=== -> 타입까지 비교 하기 때문에 더 정확히 나옴 
중요!) == 많이 안쓰고 자바스크립에선 === 을 많이 쓴다. 
+) && 연산자 : 모든 값이 true인지 확인하지만 첫번째가 이미 false이면 확인할 필요가 없다. 

Type [undefined, null, boolean, number, string, object, function, array, Date, RegExp ..] 
-자바스크립은 타입은 여러개 존재하는데 타입을 쓰는 것이 없다. 
- 변수의 타입은 실행타임에 결정된다. 타입이 나중에 결정되는 것이다. 
- toString.call 통해서 자바스크립타입을 확인 할 수 있다. 

<javascript 변수 / 타입 (출처 : MDN)>
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

## 20180523

함수 
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

## 180524 
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

## 180526

#### DOM (Document Object Model)

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

#### 180528

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
#### <라이프 사이클>
서블릿과 같다.

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
#### <JSP 문법>

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
#### <JSP 내장객체>
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



 

   
     
















 
 
 
 
 
