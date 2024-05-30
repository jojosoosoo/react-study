# Swiper 활용

: [Swiper](https://swiperjs.com/react)

## 1. 설치

- `npm i swiper`
- public/index.html의 link/script 태그 제거

## 2. 기본 활용

- `import { Swiper, SwiperSlide } from "swiper/react";`
- `import "swiper/css";`

## 3. 기능 추가

- `import { EffectFade, Autoplay } from "swiper/modules";;`
- `import "swiper/css/effect-fade";`
- `import "swiper/css/autoplay";`
- 옵션을 지정

```js
<Swiper effect={"fade"} autoplay={{ delay: 1000, disableOnInteraction: false }} modules={[EffectFade, Autoplay]}>
  <SwiperSlide></SwiperSlide>
</Swiper>
```

## 4. 옵션은 별도로 작성하기를 권장

```js
// Swiper의 옵션은 별도로 변수에 담아서 관리 추천
const swiperOption = {
  speed: 500,
  effect: "fade",
  autoplay: { delay: 1000, disableOnInteraction: false },
  modules: [EffectFade, Autoplay],
  onInit: (swiper) => {
    // 매개변수 swiper는 현재 생성된 슬라이드를 말함
    swiper.autoplay.stop();
    swLogoSlide.current = swiper;
  },
};

<Swiper {...swiperOption}></Swiper>;
```

# JS 31장

```txt
정규표현식은 문자열패턴 검색
- 문자열에 대한 처리가 PG에서 중요
- 문법이 복잡하여서 보통 정규표현식은 검색해서 사용하는 것이 관례
- yup 라이브러리를 많이 활용
- 조건 /^\d{3}-\d{4}-\d{4}$/
```

# JS 32장

```txt
활용도가 높지만 간단

const go = new String();    (X)

length: 길이
[1,2,3].length: 보통은 배열에서의 길이
"hello".length: 문자열의 길이

String 메서드()
"hello".indexOf("e")
"hello".includes("e")
"hello".chartAt(인덱스)
"hello".substring(2,4)
"hello".toUpperCase()
"hello".toLowerCase()
**"   he   llo    ".trim()**: 중요함 (단점: 중간공백 제거 안됨)
**"hello".replace()**: 중요함
**"hello".split(기호)**: 중요함 (기호를 이용해서 글자를 뜯어서 배열을 만듦)

```
