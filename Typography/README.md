### Typography

Typography ? 텍스트(Text)를 예쁘게 디자인 하는 개념  

### 1. font-size 

> 글씨의 크기를 나타내는 속성  

사용하는 단위 : px, em, rem

px ? 절대 단위, 해상도를 지정할 때 1920x1080 로 지정한다면, width(너비)는 1920px이고, height(높이)는 1080px

em ? 상대 단위로, em단위가 있는 곳의 폰트사이즈의 배수

rem ? 상대 단위로, root(html) em의 약어인데 문서의 기본값의 배수 => rem단위는 html의 기본값의 배수이므로, 문서 전체의 기준값에 따라 달라진다.

### 2. line-height  

> 줄 간격을 표시하는 속성


### 3. letter-spacing

> 글 사이의 간격을 조정하는 속성으로 주로 px단위를 사용한다.

### 4. font-family

> 글씨의 서체를 나타내는 속성

```css
.text {
    font-family: "Poppins", "Roboto", sans-serif;
}
```

Poppins -> Roboto -> sans-serif 계열의 서체  

font-family의 속성 값으로 3가지를 적어주게 되면 Poppins 서체가 지금 내 폰트에 적용이 될 수 있다면 해당 서체를 사용하고 그게아니라면 Roboto 서체 이 서체도 존재하지 않다면 sans-serif계열의 서체를 사용하게 된다.  

serif ? 삐침이 있는 서체 (명조체)

sans-serif? 삐침이 없고 굵기가 일정한 서체(돋움, 고딕)  

### 5. font-weight

> 글씨의 굵기를 나타내는 속성

|Font-weight Value|Style|
|------|---|
|100|Thin|
|400|Regular|
|700|Bold|

### 6. color

> 글씨의 색상을 나타내는 속성

hex ? #191a1c => RGB 순서대로 16진수로 변환하여 00~ff 두자리씩 표기한다.

rgb ? rgb(25, 26, 28) => 각 red, green, blue를 나타내며 0 ~ 255 사이 숫자를 입력할 수 있다.

rgba ? rgba(25, 26, 28, 1) => red, green, blue, alpha 값 여기서 alpha는 0.0(완전 투명), 1.0(완전 불투명) 사이 값을 줄 수 있다.