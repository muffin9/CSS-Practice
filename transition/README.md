### Transition

> 해당 태그에 애니메이션을 줘서 자연스러운 변화를 주는 속성  

```css
transition: property duration timing-function delay
```

transition의 property, duration은 필수값 / timig-function, delay 는 선택 값이다.

`timing-function `

> 트랜지션의 중간값을 계산하는 방법을 결정

1. ease-in : 처음에는 천천히 -> 나중에 빨리 변경

2. ease-out : 처음에 빨리 -> 나중에 천천히 변경

3. ease-in-out : 위 ease-in, ease-out 합친 개념

4. cubic-bezier() : 직접 내가 가속도를 제어 할때 사용 (수학을 못하니.. https://cubic-bezier.com/#.17,.67,.83,.67 에서 테스트 한 이후 사용하자)  

---

