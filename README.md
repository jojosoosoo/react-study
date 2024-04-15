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
