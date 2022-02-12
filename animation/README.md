### animation

> animation vs transition ? 애니메이션을 주고 싶을때(자유도가 더 큼) vs 요소의 부드러운 전환  

animation 관련 세부 속성  ?

1. name

```css
/* 애니메이션 선언! */
@keyframes move-box {
    from {
        top: 0;
        background-color: #0066ff;
    }

    to {
        top: 200px;
        background-color: #ff4949;
    }
}
```

> 애니메이션의 동작을 from(시작) - to(종료)  or  0% - 50% - 100% 로 %단위로 나눠서 선언해줄 수 있다.  


2. duration

```css
.box {
    animation-name: move-box;
    animation-duration: 2s;
}
```

> 애니메이션 지속시간

3. timing-function  

```css
animation-timing-function : ease-in
```

> transition 에서도 줄 수 있는 속성인 timing-function 애니메이션에도 적용할 수 있다.  

4. delay

```css
animation-delay: 1s
```

1초후에 애니메이션 동작!  

5. iteration-count  

```css
animation-iteration-count: infinite;
```

> 무한으로 애니메이션 동작

6. direction  

```css
animation-direction: alternate;
```

> 애니메이션 동작 방향 설정 alternate 값은 번갈아 가면서 애니메이션 동작

