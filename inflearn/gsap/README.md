# GSAP (지샵)

- Javascript Animation

## Basic [Link](https://gsap.com/)

>

- GreenSock(그린삭) Animation Platform 회사에서 만든 라이브러리이다.
- 오래된 역사를 가지고 있으며 커뮤니티가 잘 확성화 되어있는 편이다. (Carls 강의[creativecodingclub.com])
- 브라우저에 크로스브라우징 지원한다.
- 기본 코어는 무료, 그 외 유료 플러그인들이 있다.
- 구버전에는 TweenLight, TweenMax, TimelineLite, TimelineMax 객체를 사용했다. 현재는 통합해서 gsap 이라는 통합된 단일 객체를 사용한다.
- gsap 엔진에서 제어할 수 있는 속성은 다음과 같다.

  - Create Animations
  - Config Settings
  - Register plugins, eases, and effects
  - Global control over all animations

- Tweens : 애니메이션의 단위를 말하며 `gsap.to()`, `gsap.from()`, `gsap.fromTo()` 메서드를 사용할 수 있다.
  - tween 메서드 사용시 javascript로 엘리먼트에 인라인 스타일을 수정한다.
    - ⚠️ style을 변경하면 변경할 때마다 브라우저가 리렌더링 하려고 하므로 브라우저 성능 향상이 필요하다면 css animation이나 transform을 사용하는 것을 권장한다.
  - (option) repeat : [number]반복횟수 설정 (-1 설정시 무한반복)
  - (option) delay : [number]지연시간
  - (option) repeatDelay : [number]반복설정시 지연시간 설정
  - (option) yoyo : (=animation-direction: alternate) [boolean]되돌아오는 설정
  - (option) ease : [string]가속도를 설정 (default: ease)
    - [docs](https://gsap.com/resources/getting-started/Easing)
    - bounce (튀기는 효과), powe1 등
  - (option) ٭stagger : [object]단일 트윈에서 여러 대상의 시작 시간을 오프셋 설정
    - 2버전에서는 staggerTo(), staggerFrom() 과 같은 형태로 사용했으며(더 이상 사용되지 않는다.), 3버전에서는 단일 객체에서 option으로 사용한다.
    - each : [number] 각 애니메이션 간격 설정
    - amount : [number] 애니메이션의 총 시간 설정
    - from : [string] start | end | center(중간부터) | edges(가장자리부터)
  - (optiion) paused: [boolean]
- Staggers Option : 각 객체 애니메이션에 delay 설정
- Timeline :`gsap.timeline();` 을 사용하여 timeline 객체를 받아 tweens를 순서대로 실행되도록 한다.

  - Example

  ```js
  const tl = gsap.timeline();
  tl.to("green", { duration: 1, x: 200 });
  tl.to("orange", { duration: 1, x: 200, scale: 0.2 });
  tl.to("grey", { duration: 1, x: 200, scale: 2, y: 20 });
  ```

  - methods

  ```js
  const tl = gsap.timeline();
  tl.play(); // 시작
  tl.pause(); // 멈춤
  tl.resume();
  tl.reverse(); // 역방향 시작
  tl.restart(); // 다시시작
  ```

## Advanced

-

## ScrollTrigger

## SVG
