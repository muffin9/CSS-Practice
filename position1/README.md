### Position

🌟 Type -> 기준점 중요!(static, relative, absolute, fixed, sticky)  

1. static

position의 default Type은 static!  

2. relative  

relative는 자기자신이 기준점이 되는데, float와 붕뜬 속성은 같지만 자신이 원래 있던 위치는 기억되므로 형제 뒤의 요소들이 앞으로 밀려나는게 아닌 원래 있던 그 요소에 위치함  

3. absolute

특정 요소에 position: absollute;를 먹일시 float 속성과 매우 비슷하게 동작하는데, 

1. absolute 요소의 부모 요소는 해당 요소가 없다고 생각함
2. display -> block 으로 바뀐다.
3. 길막을 하지 못하는 Block

`absolute vs float ? `

1. absolute의 요소는 float의 inline 으로 보여지는 속성은 가지지 않는다.  
2. 기준점 요소를 개발자가 정할 수가 있음 (부모 요소의 속성이 position이 static이 아니라면 부모 요소를 기준으로 따르지만 부모 요소의 position이 static이라면 부모의 부모 요소 position이 static이 아닌 값을 찾아 최상위 부모요소까지 올라간다.)  

4. fixed

fixed는 viewport 사이즈 기준으로 기준점을 잡는다.  

`viewport ? 브라우저 창의 전체 크기  `
