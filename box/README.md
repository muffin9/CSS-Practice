### Box model ?

html 요소들은 Box가 일정한 모델의 형태로 구성되어 있기 때문에 Box model이라고 칭한다.

=> html의 요소들은 css로 표현할때 결국 Box로 표현된다.  

box의 공간은 content, padding, border, margin로 이루어져 있다.

content: width, height 콘텐츠 영역

padding : 안쪽여백으로 content, border 사이의 공간을 나타내는 padding

border : 테두리를 나타내는 영역

margin : 요소와 요소 사이의 간격을 나타내는 바깥여백  

---

### Box size

```css
* {
    /* default */
    box-sizing: content-box; 
}
```

box-sizing 값을 border-box로 지정해주면 border까지의 영역을 콘텐츠로 하겠다 라는 의미!  
기존 default인 content-box값은 border,padding 영역을 포함하지 않는 콘텐츠의 영역만됨

(box-sizing: border-box => box content = content + padding + border)  

---

### Box  

display : box의 형태를 결정하는 요소로, 요소를 화면에 어떻게 표시할지 사용하는 속성이다.

`1. Block`

- 따로 width를 선언하지 않은 경우, width = 부모의 content-box의 100%  

- 따로 width를 선언하는 경우, 남은 공간은 margin 으로 자동으로 채운다.  

- 따로 부모의 height를 선언하지 않을 경우, 자식 요소의 height 합 = 부모의 height

`2. Inline`

Block 속성과 달리 우리가 글을 쓰는거처럼(가로배치) 옆 공간이 없을때는 공간이 아래로 내려가서 추가함  

width, height, top, bottom 사용불가 ? Why ? inline의 흐름을 방해하는 속성들이기 때문!

`3. Inline Block`  

Inline + Block의 속성이 부분적으로 합쳐진 속성으로, 가로로 배치함과 동시에 영역을 잡을 수 있다.
