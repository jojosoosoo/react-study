# css 최적화

# js Syntax 1장

프로그래밍: 요구 사항을 분석하고**(개인별로 작성: 의사 코드**),
syntax를 이용하여 적절한 자료구조+적절한 함수를 이용하고,
흐름을 제어하여 요구 사항을 만족 시킴

**syntax** (구문): 약속된 문법
**Interpreter**(번역): 갤럭시 AI/웹브라우저

# js Syntax 코드 위치

1. inline 방식

```html
<div class="wrap" onclick="alert('안녕');"></div>
```

2. 태그 방식

```html
<script>
  alert("반가워");
</script>
```

3. 외부 파일 방식

```html
<script src="./js/script.js">
  alert("반가워"); // 이거 실행 안됨
</script>
```

# Swiper Slide 적용해 보기

- Slide를 직접 코딩하지 마세요.
- 사용법을 배운다.
- Swiper(https://swiperjs.com/), Slick(https://kenwheeler.github.io/slick/), BxSlide(https://bxslider.com/)가 있음

## 1. Swiper Slide 적용시 주의사항

- html 로드 완료 및 이미지 로드 완료 후 실행 권장

```js
wondow.addEventListner("load", function () {
  // 실제 슬라이드 코드 배치
});
```

# js 2장

```js
 mp3  실행하려면? mp3 Player
 .hwp 실행하려면? 한글 Player

  javaScript 뭐지 ?


  publisher : 웹브라우저용 프로그래밍 언어 (html, css 다룬다)
  FE        : node.js (웹브라우저용 pg 아니고, pc 용 프로그래밍 언어)
              서버(dothome... db... html, css ...)

  웹 브라우저 player 마다 다 다르다.
  IE, Chrome, Opera, Safari..... (모두 다 다르다. Syntax )
  예) 메뉴하나를 만들어도 다시 각각에 웹브라우저에 맞게 마이그레이션을 해야.



  ES6

  렌더링 (목표는 html, css, js 로 문서 만들기)

   SSR (Server Side Redering)
    : php, spring (WAS), Next.js

   CSR (Client Side Redering) 이 있어요.
    : React, Vue, Angular ..

   Ajax (아작스, 에이젝스..) : 데이터(json) 통신
     : 비동기 (Request 요청  Response 회신) / 동기 구분
     : XML Http Request (XHR 통신)
     : vanila JS / pure JS (fetch/async await)     <=====>    jQuery (ajax)


     Node.js 하실 수 있나요?
      서버(Express.js), DB(MongoDB, MySql) 가능합니까?

     SPA : Single Page Application
     CBD : Component based Developement

     객체 지향
     : 모든 코드의 시작은 객체로 설계하여 전개한다.

     예) 기획자 : xls 로 제공한다.
         - 인터파크 상품(최상단 배치되는 제품의 정보를 노출)
         - 상품의 기본 정보
          : 할인율, 가격, 제목, 이미지 보여주면 되겠다.
          : 제품상세 정보로 이동하는 경로를 제공

         디자이너
         - UI 및 UX 배치

         BE 개발자
         - 제품의 정보를 DB 저장해둠. (일부만 Response )

         FE 개발자 :
         const Good = {
           ratio : 할인율,
           price : 가격,
           title : 제목,
           pic  : 이미지주소,
           link : 제품주소
         }

         const 객체명 = {
            속성명 : 속성값,
            기능   : function(){ 기능 }
         }


         Const TodoList = () => {
           const gogo = (e) => {
             alert ("클릭")
           }
           return (
              <>
                <div className="a" onClick="gogo">
                  ~~~~
                 </div>
              </>
            )
         }


     프로토타입 기반 : 프로토타입(유전자)를 상속받아 덧댄다.

     Babel 이란 : 현재 최신 코드를 옛날 코드로 변환해 준다.
```

# Swiper Slide 적용해 보기 2

- 데모사이트의 core 메뉴를 통해서 참조
- 기본 css와 js 파일은 CDN으로 참조

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css"
/>
<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
```

- 기본형 코드를 작성해서 원하는 영역에 배치
- 슬라이드 개수만큼 swiper-slide div를 만듦

```html
<div class="swiper 원하는 이름">
  <div class="swiper-wrapper">
    <div class="swiper-slide">내용</div>
    <div class="swiper-slide">내용</div>
    <div class="swiper-slide">내용</div>
  </div>
</div>
```

- css로 `원하는 이름`을 찾아서 width, height를 100% 주기
- css로 `원하는 이름`에 절대로 display 등을 넣으면 안됨

# Swiper Slide 적용해 보기 3

- 외부 데이터 연동 (json)
- 데이터의 구조를 설계
- json: javascript Object Notation

```json
[
  { "키": 값, "키": "값", "키": "값" },
  { "id": 2, "pic": "b2.png", "url": "#" },
  { "id": 3, "pic": "b3.png", "url": "#" },
  { "id": 4, "pic": "b4.png", "url": "#" }
]
```

# Swiper Slide 적용해 보기 4

- 비동기 호출하기(vanila/pure js)
  : BE와 협업시 활용
- fetch를 활용 가능
- async await 활용 가능

# js 3장

```txt
DOM(Document Object Model)
   - html 을 읽고, 수정 등등의 조작을 하는 함수 (DOM API)
     document.querySelector(".wrap")

    클라이언트 사이드 API
    DOM, BOM, Canvas, XMLHttpRequest, fetch
    requestAnimationFrame, SVG, Web Storage,
    Web Component, Web Worker 등..

    Node.js   설치를 하면 자동으로
    npm 설치 됩니다. Node Package(js 소스) Manager
    https://www.npmjs.com/

    npm install 패키지명@버전
    node -v
    npm -v

    nvm (Node.js 의 버전을 자유롭게 변경하고, 설치)

    yarn install 패키지명@버전
```

# Swiper Slide 적용해 보기 5

- 외부 js 파일 이용

```html
<script src="./js/파일명.js"></script>
```

```js
window.addEventListener("load", function (){
  // 내용 작성;
}
```

- swiper에 보여줄 데이터를 외부 .json 파일로 연동
  : 자료(데이터)를 만들어 주는 동료가 BackEnd임
  : BE와 협의가 필요 (협업의 기본)
  : 초기에는 가짜데이터(Dummy, Mockup)를 가지고 작업

```json
[
  { "키명": "키값" },
  { "키명": "문자열" },
  { "키명": 55},
  { "키명": true},
  { "키명": []}
  { "키명": {} }
]
```

```json
[
  {
    "id": 1,
    "pic": "b1.png",
    "url": "#",
    "title": "AI 헬스케어의 <br/> 마일스톤을 찍다"
  },
  {
    "id": 2,
    "pic": "b2.png",
    "url": "#",
    "title": "카카오브레인의 <br/> 연구문화"
  },
  {
    "id": 3,
    "pic": "b3.png",
    "url": "#",
    "title": "PathFinder 2기의 <br/> 언어모델 활용기"
  },
  { "id": 4, "pic": "b4.png", "url": "#", "title": "칼로의 꿈 <br/> 시리즈 ③" }
]
```

- json 데이터를 이용해서 자료 추출
  : 외부 주소를 통해 자료를 불러들이기 위해 fetch를 알고 적용
  : 더불어 크롬 개발자 도구(F12)의 Network 탭을 알아야 함
  : 옵션으로 Fetch/XHR을 선택할 수 있어야 함
  : request와 response를 구별하여 파악할 수 있어야 함

```js
fetch("주소").then().then().catch();
```

```js
fetch("주소")
  .then((결과) => {
    const 접속결과 = 결과.json();
    return 접속결과;
  })
  .then()
  .catch();
```

```js
fetch("주소")
  .then((결과) => {
    const 접속결과 = 결과.json();
    return 접속결과;
  })
  .then(function (최종자료) {
    // 하고 싶은 일 마음대로....
  })
  .catch();
```

```js
fetch("주소")
  .then((결과) => {
    return 접속결과;
  })
  .then((최종자료) => {
    // 하고 싶은 일 마음대로....
    // 우리가 할 일을 진행한다.
  })
  .catch((오류) => {
    // 오류처리
  });
```

- 추출된 데이터로 html 생성
  : 백틱(``)을 적극적으로 사용

```js
for (let i = 0; i < result.length; i++) {
  const data = result[i];
  // 템플릿 문법 필요 (html)
  const test = `<div class="swiper-slide">
          <a href="${data.url}" style="background:url('./images/${data.pic}') no-repeat center; background-size: cover;">
            <p class="slide-title">
              ${data.title}
            </p>
          </a>
        </div>`;
  slideTags += test;
}
```

: html 배치

```js
// 원하는 장소에 출력해 보자.
const whereTag = document.querySelector(".topslide .swiper-wrapper");
whereTag.innerHTML = slideTags;
```

- swiper를 작동시킴
  : html 완료 후 슬라이드 생성

```js
// DOM을 다루려고 하는 목적인 경우
window.addEventListener("load", function () {
  // 1. 외부에서 자료를 불러온다.
  const dataUrl = "./apis/topslide.json";

  fetch(dataUrl)
    .then((response) => {
      // Step 1. 자료 받아서 json 변경하기
      // 토큰을 js의 데이터로 변경하기
      const data = response.json();
      // 변환된 결과를 돌려주기
      return data;
    })
    .then((result) => {
      // Step 2. json 변경된 데이터 활용하기
      // 전체 글자 모음
      let slideTags = "";

      for (let i = 0; i < result.length; i++) {
        const data = result[i];
        // 템플릿 문법 필요 (html)
        const test = `<div class="swiper-slide">
          <a href="${data.url}" style="background:url('./images/${data.pic}') no-repeat center; background-size: cover;">
            <p class="slide-title">
              ${data.title}
            </p>
          </a>
        </div>`;
        slideTags += test;
      }

      // 2. 자료를 이용해서 슬라이드에 배치할 html을 만든다.
      // 원하는 장소에 출력해 보자.
      const whereTag = document.querySelector(".topslide .swiper-wrapper");
      whereTag.innerHTML = slideTags;

      // 3. html 완성후 swiper 를 생성한다.
      // 기본코드를 넣어보자.
      var topSlide = new Swiper(".topslide", {});
    })
    .catch((error) => {});
});
```

# Swiper Slide 적용해 보기 6

- [옵션](https://swiperjs.com/demos#autoplay)
  : loop
  : autoplay
  : effect
  : speed
  : pagenation(https://swiperjs.com/demos#pagination)
  : 페이지네이션 디자인 수정하기 참조!

```css
.bannerslide .swiper-pagination {
  bottom: 30px !important;
}
.bannerslide .swiper-pagination-bullet {
  width: 4px !important;
  height: 4px !important;
  background: #ffffff !important;
  opacity: 0.7 !important;
  border-radius: 4px !important;
  transition: width 0.3s;
  margin: 0 2px !important;
}
.bannerslide .swiper-pagination-bullet-active {
  background: #ffffff !important;
  opacity: 1 !important;
  width: 20px !important;
}
```

# js 4장

- var 변수명 = 변수값;
- let 변수명 = 변수값;
- const 변수명 = 변수값;

```txt
  호이스팅(hoisting)은 변수, 함수를 선언하지 않았는데도 사용 가능 (hoisting이 일어나지 않도록 주의: var 쓰지 말자)
```

# css의 opacity와 position의 이해

- opacity는 DOM의 내용까지도 투명도가 적용됨
- position
  : position 중에 absolute로 픽셀 위치 설정하는 경우 주의
  : 반드시 position 코드가 바깥 영역에도 있어야 함
  : position 중에 fixed는 웹 브라우저를 기준으로 배치
  : fixed는 반드시 left, top, right, bottom을 주어야 함
  : fixed는 보통 z-index를 줌
  : fixed는 높이에 반영이 되지 않으므로 주의 (레이아웃 배치 문제)

```css
대상 {
  position: relative;
}
대상 {
  position: absolute;
}
대상 {
  position: fixed;
}
```

- 주의사항

```css
.box-wrap {
  position: relative;
  margin: 0 auto;
  width: 600px;
  height: 300px;
  background: orange;
}
.box {
  position: absolute;
  right: 80px;
  bottom: 20px;

  width: 200px;
  height: 200px;
  background: red;
}
```

# js 윈도우 스크롤의 위치 알아내기

```js
window.addEventListner("scroll", function () {
  // 하고 싶은 일
});
```

```js
window.addEventListner("scroll", function () {
  // 스크롤 바의 위치
  const scY = window.scrollY;
});
```

## js로 css의 클래스 동적으로 활용하기

```js
// DOM 찾아서 변수로 레퍼런스 하기
const tags = document.querySelector(".클래스명");
// DOM을 이용해 선택한 곳에 적용된 css 클래스 목록 추가
tags.classList.add("클래스명");
// DOM을 이용해 선택한 곳에 적용된 css 클래스 목록 제거
tags.classList.remove("클래스명");
// DOM을 이용해 선택한 곳에 적용된 css 클래스 목록 추가/제거
tags.classList.toggle("클래스명");
// DOM을 이용해 선택한 곳에 적용된 css 클래스 목록 포함 여부
tags.classList.contain("클래스명");
```

# js의 함수란? 1

- 동일한 코드가 두 번 이상 반복되면 함수를 만들려고 노력할 것
- 반복되지 않아도 하나의 기능이 너무 복잡하면 함수를 만들려고 노력할 것
- 복잡하지 않아도 코드가 너무 길어지면 함수로 묶어주려고 노력할 것
- 실행의 결과가 그때그때 다른 경우에도 함수를 만들 것

```js
// 함수 선언 (함수 만들기)
function 적절한동사() {
  // 하고 싶은 일 작성
}

// 함수 호출/콜 (함수 사용하기)
적절한동사();
// 예 (함수 체이닝)
fetch().then().then().catch();
```

- 함수는 무조건 한 개의 값을 리턴(return)하도록 규정
- return: 함수 실행() 후 값을 돌려주는 것

```js
function 함수명() {
  // return undefined (몰래 작성됨)
}
함수명();
```

# JS 5장

```txt
코딩에서 값이라고 할 수 있는 것은
  변수에 할당(보관한)된 결과를 말한다.

  변수란? 컴퓨터 공간에 이름을 붙여둔 방 한개

  표현식이

  평가(식을 해석해서 값을 생성하고 참조하는 것)된
   결과를 말한다.


   리터럴 이란?
   사람이 이해할 수 있는 문자 또는 약속된 기호를
   사용해서     값   을    생성하는 표기법

   리터럴은 값을 평가해서 코드에 활용하기 위한 문법


  "function"
  var function

  function gg(){}

  표현식 expressioin
  : 리터럴 값으로 평가가 되면 OK!
     5  숫자 리터럴 값으로 평가가 되면 OK!
     "안녕" 문자열 리터럴 값으로 평가가 되면 OK!

     var num = 5;
     var num:number = 5;


  문(statement) :  프로그램을 구성하는 기본단위/최소 실행단위

  {}


  var foo = x = 100
```

# js의 함수란? 2

- 동일한 코드가 두 번 이상 반복되면 함수를 만들려고 노력할 것
- 반복되지 않아도 하나의 기능이 너무 복잡하면 함수를 만들려고 노력할 것
- 복잡하지 않아도 코드가 너무 길어지면 함수로 묶어주려고 노력할 것
- 실행의 결과가 그때그때 다른 경우에도 함수를 만들 것

- 함수 정의문

```js
function 함수이름() {
  할일;
}
```

- 함수 실행(호출/call)문

```js
함수이름();
```

# js의 함수의 매개변수란? 3

- 초기 기능 즉, 함수를 정의하기 전에 기능상 자주 변하는 데이터를 고민
- 기능은 스크롤시 특정 위치보다 커지면 css 추가하기
- 이전 코드는 좋지 않은 코드라고 생각
- 함수는 스스로 지역 즉, Local 영역(Scope)에서 처리되는 것이 좋다고 봄
- `처리`라는 말은
  : 변수를 찾는다든가,
  : 잘못된 값이 전달되어서 오류가 나는 것을 방지하는 것을 말함

```js
// 홍길동에게 줄 함수
const a = 5;
const b = 6;
function 나누기(_num1, _num2) {
  if (_num2 === 0) {
    alert("나눗셈에서 0은 안됩니다");
  }
  return _num1 / _num2;
}
나누기(a, b);
```

# JS 6장

````txt
   데이터 타입 ( Data Type ) : 자료형
   타입 이라는 말이 자료의 형태
   JS의 리터럴로 처리될 수 있는 자료의 종류

   타입 스크립트 : 데이터 종류를 표현해 주는 방식

    '5'   , "55", `555`
    'a'   , "ab", `55555`

    "안녕
      반가워
    "
    `안녕 ${100}
      반가워
    }
    `

    undefined 와  null 헷갈려요.
    const a = undefined; (모르겠다.)
    const b = null; (개발자가 직접 진짜 값이 비었다고 알려줌)

    Symbol 은 중복되지 않는다고 보장하는 값 타입
    Symbol()

    데이터 타입 ( Data Type ) : 자료형
    불변성(immutable) : 데이터 값이 변경될 수 없다.
    데이터는 immutable 해야 합니다.
    상태는   immutable 해야 합니다.
    state는  immutable 해야 합니다.

    1 = 1;


    가변성(mutable) : 데이터 값이 변경될 수 있다.


    원시데이터 6가지가 있는데 immutable 한 데이터 타입입니다.

    number   1
    string   'a'
    undefined undefined
    boolean    true, false
    null       null
    symbol     Symbol() 만들어진 값은 변경 불가

     복합형 데이터 객체
     객체는 원시데이터를 모아서 저장하고 관리하는 것.

    // 묶어라, Block
    const hong = {
        age: 20,
        marry : true
     }


     // 내가 c 라는 이름으로 저장할 거야
     // c 라는 공간은 글자를 보관할 거야
     // 그러니, 공간을 좀 마련해 줄래?

     // C 를 사용하는 프로그래머는
     char c = 'a'
     int num = 5;

     // js 를 사용하는 프로그래머는
     const c = 'a';
     const num = 5;

     // ts 를 사용하는 프로그래머는
     const c:string = 'a';
     const num:number = 5;


     // 오늘, 그리고 다음을 위해서 꼭 알아야 하는 단어

     1. 데이터 타입 : 자료(리터럴 값)의 종류

     2. js 에서는 값 리터럴에 따라 변수의 종류를 타입추론 한다.

     3. 타입을 추측해서 프로그래머에게 물어보지않고 타입을 변경한다. (암묵적 타입변경)

        let a = 1;
        a = "안녕";

        2번 3번은 원하지 않는 결과를 언젠가 실행됩니다.
        의도하지 않은 오류를 일으킨다.

        TypeScript

        let a:number = 1;
        a = "안녕"; // 오류 발생

  // 코딩 할 때 스스로 고민해 보자.

   1. 꼭 필요한 경우인지를 파악하고 변수를 만들자.
   2. 변수 유효범위는 좁게 (블록을 가능하면 쓰자)
   3. 전역변수는 가능하면 만들지 말자.
   4. 변수는 상수를 쓰세요.

      let a = 1; (X)

      const count = 1;

      {
        let count = 2;
      }
      ```
````

# 함수의 이해 7번

1. 함수를 만들어야겠다고 판단하는 케이스

- 동일한 코드가 두 번 이상 반복되면 함수를 만들려고 노력할 것
- 반복되지 않아도 하나의 기능이 너무 복잡하면 함수를 만들려고 노력할 것
- 복잡하지 않아도 코드가 너무 길어지면 함수로 묶어주려고 노력할 것
- 실행의 결과가 그때그때 다른 경우에도 함수를 만들 것

2. 왜 화살표 함수를 만들지?

- 트랜드를 쫓아가자 (뭐 좀 있어보임)
- 코드 해석하기 더 어려워짐

<화살표 함수 연습>

```js
function say() {
  console.log("안녕", this);
}
```

: Step 1.

```js
say() {
  console.log("안녕", this);
}
```

: Step 2.

```js
const say = () => {
  console.log("안녕", this);
};
```

<매개 변수가 있는 경우>

```js
function say(_who) {
  console.log("안녕", _who, this);
}
```

: Step 1.

```js
say(_who) => {
  console.log("안녕", _who, this);
}
```

: Step 2.

```js
const say = (_who) => {
  console.log("안녕", _who, this);
};
```

- this를 정확히 지정하기 위해 활용
  : 화살표 함수를 사용하면 일반적으로 큰 고민 없이 사용하면 됨
  : 하지만, 함수 안에 this를 작성하게 되면 상황이 달라짐
  : 화살표 함수에서 this는 window를 가리킴
  : 결론은, **화살표 함수에서 this를 사용한다면 console.log(this) 확인 필수!**
  : 되도록이면 그냥 쓰지 마셈

  : 화살표 함수는 예전 일반 함수에서 window를 참조하지 못하는 문제를 해결함

```js
// this의 차이 (어렵지만 이해해야 함)
const btWrap = document.querySelector(".bt-wrap");
// 일반 함수는 this가 타이핑이 된 곳을 가리킴
btWrap.addEventListener("click", function () {
  console.log(this);
});
// 화살표 함수는 this가 window를 가리킴
btWrap.addEventListener("click", () => {
  console.log(this);
});
```

# 배열의 이해

- [요소, 요소, 요소, 요소]
  : 요소로 담을 수 있는 자료형은 7가지
- 배열의 속성(배열을 위한 특별한 변수)은 1개
  : length (요소의 개수)
- 배열의 메서드(배열을 위한 특별한 함수)는 너무 많음
- 상당히 많은 메서드(배열을 위한 함수)가 있음
  : 배열.forEach((요소)=>{}), 배열.map((요소)=>{}), 배열.filter((요소)=>{}), 배열.find((요소)=>{})
- 배열의 요소를 하나씩 접근해서 활용하기
- 정화섭 바보 카멜케이스 써야지 ( 배열.forEach() )

```js
// 배열이라면 반복하자.
result.forEach((item) => {
  const tag = `<a href=${item.link} class="list-box">
        <div class="list-box-img br-20" style="background: url('./images/${item.imgpath}') no-repeat center; background-size: cover"></div>
        <div class="list-box-cate">
          <img src="./images/icon/${item.icon}" alt="${item.category}" />
          <span style="color:${item.txtcolor};">${item.category}</span>
        </div>
        <p class="list-box-title">${item.title}</p>
        <span class="list-box-day">${item.day}</span>
        </a>`;
  allTag = allTag + tag;
});
```

# JS 7장

```txt
operator (연산자)

   이  항   :   2개의 항목 을 처리하는 연산자 값만들기
   삼  항   :   3개의 항목 을 처리하는 연산자 값만들기
   단  항   :   1개의 항목 을 처리하는 연산자 값만들기

   +   -    *    /   % (모듈러 연산자)

   5 % 3 = 2 (나누고 난 후 나머지 값, 게시판 목록..)

    단  항   :   1개의 항목 을 처리하는 연산자 값만들기

    let a = 1;
    a = a + 1;
    a++;    // 원 값에 1을 더하라
    ++a;    // 원 값에 1을 더하라
    --a;    // 원 값에 1을 빼라
    a--;    // 원 값에 1을 빼라
    for(let i = 0; i < 10; i++) {
    }
    장바구니 개수 추가
    let bucket = 0;
    bucket++;

    알고리즘 공부
    let a = 1;
    let b = a++;   // b?  1   a = 2
    let b = ++a;   // b? 2

   1 + 2 = 3
   '1' + 2 = "12"
   글자도 더할 수 있다.

   const filePath = "./images/"
   const fileName = ".jpg";
   for(let i = 0; i < 10; i++) {
      const img = filePath + i + fileName;
      const img = "./images/" + 0 + ".jpg";
      const img = "./images/" + 1 + ".jpg";
      const img = "./images/" + 2 + ".jpg";
   }

    처음 코딩 배우면 어려워 하는 것

    문법
        []  ....
        for  문....
        할당 문...
        let num = 0;
        num = num + 1;
        num ++;
        num += 1;

==================== 적절한 구조를 어떻게? ====
    변수, 함수, 객체 구조?


   1 == '1'        같다 (true)
   암묵적으로 타입 변환 시켜서 진행 :  나중에 오류의 원인
   절대로 사용하지 마세요.


   1 === '1'  다르다.
     1. 먼저 데이터 종류 (data type) 비교합니다.
     2. 데이터 값 (data value) 비교합니다.

     !==



     (조건) ? 참실행 : 거짓실행

     (level > 10) ?  <div>주인님</div>    :   <div>일반회원</div>

     if(isLogin) {

        <div>"반가워"</div>

     }else{

        <div>회원가입</div>
     }

     const 객체 = {
         프로퍼티명 : 프로퍼티값
     }
     객체 in 프로퍼티명
     delete 객체.프로퍼티명;

     const sw = new Swiper(".slide", {} )

     const a = (1 + 10) * 100

```

- 함수 리턴의 이해

```txt
1. 함수 정의
     function 함수이름(매개변수) {
     }

2. 함수 호출
     const gogo = 함수이름(100); // gogo 에는 undefined;

3. 리턴이 여러개인 경우
  : return 의 의미는 함수 결과값 돌려주기
  : return 은 함수 종료하기

     function 함수이름(매개변수) {
        return 1;
        return 2; // 영원히 실행이 안됨.
     }
```

# JS 8장

```txt
제어문은 조건에 따라서 코드 진행 방향이 결정된다

    고차함수 란 ? 함수의 매개변수로 함수를 전달한다.
    window.addEventListener(문자열타입, 함수타입)
    글자, 숫자, boolean, null, undefined, symbol
     객체 : [], funciton, {} ...

    버스를 기다린다.
     300 번은 5분마다 온다.  둘다 시내로 가요
     700 번은 10분마다온다.

     if(300 번 === 버스번호) {

     }else if(조건) {

     } else {

     }

     조건문으로 if 와  switch 문이 있다.
     주로~~~~   if 문을 우선 활용하세요.

     그리고, 나중에 리액트 하실 때, reducer 라는 것을 할때
     switch 를 그때 다시 접근하시길 권장해요.

     for 문은 반복 횟수가 명확할 때 주로 사용
     while 문은 반복 횟수가 불명확 할 때 주로 사용

     for (var i = 0; i < string.length; i++) {

           if(i === 3) {
             break;
           }

           console.log("안녕 ^^")
    }

> 반복을 대체할 수 있는 다양한 기능*
>
- forEach 메서드 : 배열을 순회할 때 사용
    [1,2,3]

- for in 문 : 객체의 프로퍼티를 열거할 때 사용
    {
      age: 1,
      marry: false,
      nicName: "Chlie"
    }

- for of 문 : 이터러블(itrable : 순서가 있는)을 순회 가능
```

# JS 9장

```txt
명시적 타입 변환
 : 개발자가 타입을 강제 변환
 : 타입캐스팅

암묵적 타입 변환 (코드에러가 아니고 원하는 결과가 아닌 경우)
 : JS가 타입을 몰래 변환
 : 타입 강제 변환
 : 개발자가 결과를 예측할 수 있어야 합니다. (대비책)

:  + 연산자는
  '글자' + '글자' = '글자'
   숫자  +  숫자  =  숫자
  '글자' + 숫자   = '글자'     원칙(일단 숫자로 바꾼다.)


:  - 연산자는
   '글자' - '글자' = NaN
   숫자  -  숫자  =  숫자
  ' 5 ' - 숫자   = '글자'     원칙(일단 숫자로 바꾼다.)

  console.log(typeof 결과)


: Boolean    true/false

Falsy 한 것들을 반드시 알아야해요  결과값 false 가 나옴
  false, undefined, null, 0, NaN, ''

 if (userId) {
   alert("아이디가 있어요")
}else{
   alert("아이디가 없어요")
      }

문자열 데이터 지정 만들기
  변수 + ''

숫자 데이터 지정 만들기
  parseInt(변수)     :    정수 만들기
  parseFloat(변수)   :    실수 만들기

단축평가
 : 리액트에서 엄~~~~~~~~~~~~청 사용합니다.
 : 반드시 정말 알아야 합니다.

 : false, undefined, null, 0, NaN, ''

 - 논리곱(&&)
   true && true  결과는 true 입니다.

   "비욘세" && "디카프리오"  결과는 죄송하지만 true 가 아닙니다.
                            결과는 "디카프리오"

   const isLogin = true;
      isLogin &&  "<div>안녕</div"> 결과는 "<div>안녕</div">  출력

 - 논리합(||)

   true   || true  결과는 true 입니다.
   '10억' || '1원'    // '10억'
   ''     || '1원'    // '1원'

- 옵셔널 체이닝 나오게 된 이유  (?.)

   : Syntax 에러로 js 가 멈추고 나머지 전체 js 중지..
   var elem = null;
   var result = elem.gogo;

   : 해결하기 위해서
   var elem = null;
   var result = elem && elem.gogo;

   : Synatax 에러로 js 가 멈추지 않기를 바란다.

   var elem = null;
   var result = elem ? elem.gogo : undefined;
   var result = elem ?. gogo

- 병합연산자 (??)

const result = null   ?? "없군요"   결과값은 "없군요"
const result = "안녕" ?? "없군요"    결과값은 "안녕"
```

# JS 10장

````txt
- 객체 리터럴
   : 활용빈도 말도 안되게 높고,
   : 본인 및 타소스를 이해하려면 알아야 해요.
   : 핵심은 JS 의 모든 자료타입은 객체입니다.

   - 타입(js가 리터럴로 인정하는 자료의 종류)

   : 원시 타입
    ( string, number, null, undefined, bool, symbol )

   : 객체타입
     ( [ 원시타입들... ] ,  { 속성명:원시타입 }, function ....  )


   - 객체 구성 ( 객체가 가진 데이터를 객체 내에서 제어하겠다.)

   : 객체에 포함된 변수를 `프로퍼티/속성` 이라고 호칭
   : 객체에 포함된 함수를 `메소드/기능` 이라고 호칭
      const obj = {

        "프로퍼티명" : 원시값 또는 다른 객체,
        "프로퍼티명" : string,
        "프로퍼티명" : [],
        "프로퍼티명" : {},
        "메소드명" : function () {},
      }

    - 객체 만드는 법
       인스턴스 란 ?
          : 남에게 말해주기가 어려운 개념
          : `객체를 생성하는 방법을 활용` 해 생성한 변수를 인스턴스라고 한다.

     1. 객체 리터럴 문법 : 활용빈도 높다. const 인스턴스 = {}

     const  인스턴스 = {
         "myName"  : 5,
          myJob     : 5,
         "my-age"   : 5,
         say   : function () { this["my-age"]  },
         sayHi : () => { this["my-age"]  },
     }
     인스턴스.myName
     인스턴스["myJob"]
     인스턴스.say()
     인스턴스["say"]()
     인스턴스.gogo = "안녕"

      : 객체 리터럴 문법 보완 및 축약 (ES6)

        // 기본형
        const 인스턴스변수 = {
          프로퍼티명: 프로퍼티값 ,
          프로퍼티명: 프로퍼티값 ,
          메소드명 : function() { },
          메소드명 : function() { }
        };

        const age = 10;
        const nickName = "홍길동";

        // 외부 변수 전달 받는데    이름이 똑~~ 같다?
        const person = {
           age      : age,
           nickName : nickName
        };

        //  축약형
        const person = {age, nickName};

        // 메소드 기본형
        const person = {
           say      : function() { }
        };

        // 메소드 축약형
        const person = {
           say() { }
        };



     2. Object 함수 문법

     3. 생성자 함수 문법 : 활용빈도 높다.

     4. Object.create 함수 문법

     5. class 함수 문법 : 활용빈도 높다.
     ```
````

# 카카오브레인 블로그 사이트

- 반드시 저작권을 밝혀야 함
- 첫 화면만 연습하면 됨 (첫 화면이 가장 난이도 높음)
- 리액트 적용