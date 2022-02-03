### CSS 정리

`HTML ? ` 문서 컨텐츠를 마크업다운하는데 사용하는 개념

`CSS ? ` (Cascading Style Sheet) HTML을 예쁘고 꾸미고 스타일을 입히는데 사용  

```css
selector {
    property: value; // 속성의 값마다 세미콜론 무조건 붙여야한다.
}
```

위 선언부에 내용들은 아래와 같다.

selector : css를 적용할 선택자  
property: css 속성  
value : 속성에 대한 값  

### CSS를 적용하는 방법

1. head 태그 안에 link 태그를 사용하여 파일을 불러와 css 적용

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.0.0-alpha/css/bootstrap.min.css">
```

2. html 파일 내에서 style 태그로 css 적용

```html
<!DOCTYPE html>
<html>
<head>
<style>
    body {background-color: powderblue;}
    h1   {color: blue;}
    p    {color: red;}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

3. 인라인 방식으로 css 적용  

```html
<!DOCTYPE html>
<html>
<head>
</head>
<body style="background-color: powderblue;">

<h1 style="color: blue;">This is a heading</h1>
<p style="color: red;">This is a paragraph.</p>

</body>
</html>
```

---

### `Selectors ?  `

Selectors는 선택을 해주는 요소로 이 선택자를 통하여 특정 요소를 선택해서 스타일을 적용할 수가 있다. 선택자의 종류는 여러가지가 있는데 하나하나 살펴보자.

1. Type Selector  

html 태그 셀렉터로 css를 적용하는 법이다.

```css
p {
    color: #0066ff;
}

strong { 
    color: #ffc82c;
}
```

2. Class Selector

아래 html 태그 안에 class라는 속성을 명시하고 사용할 값(box)을 넣어주면 되는 방식

```html
<div class="box-0 box-1">1</div>
<div class="box-1">2</div>
<div class="box-2">3</div>
```

```css
.box-0 {
    background-color: red;
}

.box-1 {
    background-color: blue;
}

.box-2 {
    background-color: yellow;
}
```

box 앞의 .(마침표)에 의미는 클래스를 가리키는 녀석이라고 생각하자.  

태그 안의 class로 공백을 기준으로 여러개를 넣어줄 수가 있다. 대신 각 클래스의 값마다 중복된 값이 있을 경우 뒤에온 클래스가 덮어쓰게 된다.

맨 첫번째 div태그의 배경컬러는 파랑색이다.

3. ID Selector

html에서 id속성은 고유한 값으로 사용되어지는데 이 id속성의 값으로 css를 적용할 수 있다.

```html
<div id="box">1
</div>
```

```css
#box {
    background-color: black;
}
```

---

### `자식, 자손, 형제 선택자  `

1. 자식 선택자 - Child

parent > child : parent의 바로 아래 자식 하나만 적용

2. 자손 선택자 - Descendant

parent descendants : parent의 자식, 자손 모두 적용 (depth가 상관이 없음 모두 적용된다고 보면 됨)

3. 형제 선택자 - Sibling

parent + sibling : 형제 노드 하나만 적용

parent ~ sibling : parent 뒤의 형제 노드 모두 적용

```html
<section>
    <h1>parent h1</h1>
    <ul>
        <h1>child h1</h1>
        <li>1</li>
        <li class="active">2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li>6</li>   
    </ul>
</section>
```

```css
/* parent h1태그 값만 brown으로 변경됨 */
section > h1 {
    color: brown;
}

/* 2번째 li만 빨강 */
.active {
    color: red;
}

/* 3번째 li만 파랑 */
.active + li {
    color: blue;
}

/* 4, 5, 6번째 li만 노랑 */
.active ~ li {
    color: yellow;
}
```

---

### `구조적 가상 클래스 - Struuctural Pseudo-classes`  

```html
<section>
    <h1>parent h1</h1>
    <ol>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li>6</li>   
    </ol>
</section>
```

```css
li:first-child {
    color: #0066ff;
}

li:last-child {
    color: #ffc82c;
}

li:nth-child(3) {
    color: #ff4949;
}
```

first-child : 같은 태그 중에 맨 처음 태그에만 css 적용

last -child : 같은 태그 중에 맨 마지막 태그에만 css 적용  

nth-child(n) : 특정 태그의 n번째 태그에만 css 적용  

### `동적 가상 클래스 - User Action Pseudo-classes`  

```css
a:hover {
    background-color: #ff4949;
}

a:active {
    background-color: #592dea;
}

input:focus {
    outline: none;
    box-shadow: none;
}
```

hover : 특정 태그에 마우스를 올렸을때 동작하는 가상 연산자

active : 특정 태그에 마우스를 눌렀을때 동작하는 가상 연산자  

focus : 특정 요소를 포커싱 된 상태가 될 때 동작하는 가상 연산자  

---

👀 어떤 선택자를 우선으로 적용할까 ?  

!important > inline style > id > class > type