### Float ?

어떤 특정 요소에 float을 주게 되면 어떻게 될까 ? 

1. float 속성을 갖게된 요소는 집을 나가게 되고 부모와 뒤따라나온 형제들은 집나간 요소가 어디갔는지 알 길이 없어지게 된다.
    - 부모 속성 overflow에 hidden값을 넣어주면 된다.
    - clear: 부모속성에 가상연산자를 사용하여 새로운 요소를 추가한 다음 이 요소한테 clear 속성을 주자. (display가 block인 속성만 clear속성이 먹힌다.)

2. float 속성을 갖게된 요소는 display 속성이 Block 으로 변경이 된다. But, 길막은 하지 못하는 Block // 갖고있는 콘텐츠 내용 길이만큼 width를 갖는다.  



