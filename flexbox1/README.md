### FlexBox ?

플렉스박스는 4가지 사고 과정만 기억하자.

1. 플렉스 박스를 쓸거다라고 알려주자.  
    ```css
        display: flex;
    ```
    - 정렬하고자 하는 요소들을 감싸고 있는 부모 요소한테 display: flex; 정의
2. 가로 정렬? 세로 정렬 ?  
    ```css
        flex-direction : row;
    ```
    - 가로 방향 정렬 : row / 세로 방향 정렬 : column

> 가로 정렬인 row로 셋팅을 하게 되면 Main axis는 가로축, Cross axis는 세로축을 의미하게 된다.  

> 세로 정렬인 Column로 셋팅을 하게 되면 Main axis는 세로축, Cross axis는 가로축을 의미하게 된다.  

3. 무조건 한 줄 안에 다 정렬 ?
    ```css
        flex-wrap: nowrap;
    ```
    flex-wrap은 감싸지 않고 자식의 사이즈를 줄여서 라도 한 줄로 정렬하는 속성이다.
    (Ex. 부모 width: 1000px / 자식요소 3개 각 width가 400px일 때 flex-wrap nowrap으로 속성 설정 시 각 자식요소의 width는 250px로 변경된다.)

4. 플렉스박스를 사용하여 정렬

FlexBox는 보이지 않는 두 개의 축 Axis 가 생성된다. ( Main axis, Cross axis )  

Main axis 조정 -> justify-content 속성 사용
Cross axis 조정 -> align-items(하나의 axis)  , align-content(전체의 큰 axis) 속성 사용  

