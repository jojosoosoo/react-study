# 리액트 컴포넌트

## 1.0 컴포넌트를 왜 생성하는가?

- 프로젝트 규모에 따라 협업을 필요로 함
- 기능별로 html, css, js 별도 관리 필요

## 1.1 컴포넌트에 배치되는 내용

- JSX 배치 (리액트용 HTML 태그 class => className)
- CSS 배치 (background: url (경로 문제))
- JS 배치

## 1.2 이미지를 배치하는 두 가지 경우 (주의사항)

- 태그에 이미지를 배치한 경우
  : public/images 폴더를 참조

```html
<img src="./images/etc/logo-kakao.png" />
```

- css 배경으로 이미지를 배치한 경우
  : src/images 폴더를 참조
  : 이유- css 파일을 js 컴포넌트에서 사용하면 webpack이 압축함

```css
background: url("../images/icon/icon-search.png");
```

# JS 14장

```txt
// var : 값을 담을 공간을 마련해줘.....
// var 이름 : 값을 담은 공간에 꼬리표를 붙여줘.
var age = 15;
var nickName = "hong";

function go(){
}
console.log(age)
=
console.log(window.age)

모듈(기능별 파일코드)은 import/export 문법을 써서 변수 범위를 설정함

(Class 장 참조)
외부에서 변수 및 함수에 접근할 수 있는 권한
public: 외부 어떤 곳에서도 사용 가능
private: 외부에서 절대로 사용 불가능
protected: 허용한 대상만 사용 가능
```

## 1.3 JS를 React로 마이그레이션 진행

### 1.3.1 load가 useEffect로 변경

```js
window.addEventListner("load", function () {});
useEffect(() => {
  return () => {};
}, []);
```

### 1.3.2 querySelector가 useRef(null)로 변경

````js
const tag = document.querySelector(".bt");
const tag = useRef(null);

useEffect (()=>{
  // tag.current로 접근
  return ()=>{};
},[]);

<div ref={tag}> </div>;
```

# JS 15장

```txt
var는 없다고 생각하면 됨

const 변수이름:  값을 고정시킴
let 변수이름: 값이 수시로 바뀌어짐

const 사용하실 때 오해의 소지가 있는 경우

정군은 const 는 절대로 값이 안변한다.
값을 변경하려고 하면 에러난다.
const age = 15;
age = 100; // 에러.. conatant value...


const 객체 = {}   오해의 소지가 발생합니다.

const 정군 = {} // 이미 주소는 고정이 되어 버렸다.
정군 = "안녕"   //  주소를 교체 하려고 했다. 그래서 const 에 위배된다. 에러

// 주소를 교체하는 것이 아니고, 안쪽의 연결된 내용을 수정한다.

정군.age = 100;
정군["nicName"] = "hong guil dong";
````

# 실 업무에서 알아야 하는 상식

- nvm (Node Version Manager) 설치 및 활용
  : https://github.com/coreybutler/nvm-windows/releases
  : 설치 버전 확인 `nvm -v`
  : 설치 가능한 버전 목록 `nvm list available`
  : 설치하기 `nvm install 버전`
  : 현재 사용중인 Node 버전 확인하기 `node -v`
  : 현재 설치된 Node 목록 확인 `nvm ls`
  : 사용할 Node 버전 선택하기 `nvm use 버전`
  : Node 설치된 경로 알아보기 `which node`
  : Node 삭제하기 `nvm uninstall 버전`

- npm보다는 yarn 선호
  : Node Package Manager (node_modules)
  : package.json의 dependencies 목록 참조
  : npm이 가끔 다운로드 중 오류 발생, 소스 깨짐 현상
  : 예) 네이버 Toast UI 등...
  : npm보다 안정적인 package 관리를 위해 yarn을 활용
  : `npm install -g yarn`
  : `yarn --version`

- favicon 만들기 (디자이너 담당)
