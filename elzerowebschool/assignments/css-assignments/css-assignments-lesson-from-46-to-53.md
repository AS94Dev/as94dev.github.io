# تكليفات CSS الدروس من 46 إلى 53

## [ 6 ] تكليفات خاصة ب [ Flex Box ]

### التكليف 01

```html
<div>Elzero</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر وطوله هو 100px
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بتوسيط كلمة Elzero داخل العنصر طوليات وعرضيا بواسطة خواص ال Flex
- قم بعمل الشكل بنفس الالوان

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 10px;
  --red: #f44336;
  --green: #009688;
  --blue: #05a9f4;
  --orange: #fe5723;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

div {
  display: flex;
  width: 100px;
  height: 100px;
  justify-content: center;
  align-items: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 1.5rem;
  font-weight: 600;
  background-color: var(--white);
  color: var(--orange);
  border-radius: 50%;
  box-shadow:
    5px 0 var(--orange),
    -5px 0 var(--blue);
}
```

### التكليف 02

```html
<div class="parent">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر parent هو 600px والطول هو 300px
- قم بتوسيط العنصر parent في الصفحة بطريقة عرضية
- قم بعمل نفس العناصر بنفس شكلها وأماكنها

```css
:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 10px;
  --red: #f44336;
  --green: #009688;
  --blue: #05a9f4;
  --orange: #fe5723;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.parent {
  width: 600px;
  padding: 10px;
  height: 300px;
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  align-content: space-between;
  gap: 10px;
  background-color: var(--white);
}

.parent div {
  flex: 0 0 calc((100% - 20px) / 3);
  padding: 10px;
  height: fit-content;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--white);
  font-size: 1.5rem;
  font-weight: 600;
  background-color: var(--red);
}
```

### التكليف 03

```html
<div class="parent">
  <div class="one">1</div>
  <div class="two">2</div>
  <div class="three">3</div>
  <div class="four">4</div>
  <div class="five">5</div>
  <div class="six">6</div>
</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر parent هو 600px والطول هو 300px
- قم بتوسيط العنصر parent في الصفحة بطريقة عرضية
- قم بعمل نفس العناصر بنفس شكلها وأماكنها

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 10px;
  --red: #f44336;
  --green: #009688;
  --blue: #05a9f4;
  --orange: #fe5723;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.parent {
  width: 600px;
  padding: 10px;
  height: 300px;
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  align-content: space-between;
  /* gap: 10px; */
  background-color: var(--white);
}

.parent div {
  flex: 0 0 calc((100% - 20px) / 3);
  padding: 10px;
  height: fit-content;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--white);
  font-size: 1.5rem;
  font-weight: 600;
  background-color: var(--red);
}

.parent div:nth-child(1) {
  order: 6;
  align-self: flex-end;
}
.parent div:nth-child(2) {
  height: 50%;
  order: 5;
}
.parent div:nth-child(3) {
  order: 3;
}
.parent div:nth-child(4) {
  height: 50%;
  order: 4;
}
.parent div:nth-child(5) {
  height: 50%;
  order: 4;
}
.parent div:nth-child(6) {
  height: 50%;
  order: 1;
}
```

### التكليف 04

```html
<div class="parent">
  <div class="one">1</div>
  <div class="two">2</div>
  <div class="three">3</div>
</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر parent هو 600px والطول هو 300px
- قم بتوسيط العنصر parent في الصفحة بطريقة عرضية
- قم بعمل نفس العناصر بنفس شكلها وأماكنها

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 10px;
  --red: #f44336;
  --green: #009688;
  --blue: #05a9f4;
  --orange: #fe5723;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.parent {
  width: 600px;
  padding: 10px;
  height: 300px;
  display: flex;
  flex-flow: column;
  justify-content: space-between;
  /* align-content: space-evenly; */
  /* gap: 10px; */
  background-color: var(--white);
}

.parent div {
  padding: 10px;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--white);
  font-size: 1.5rem;
  font-weight: 600;
  background-color: var(--green);
}

.parent div:nth-child(1) {
  order: 1;
  align-self: flex-end;
}
.parent div:nth-child(2) {
  order: 2;
  align-self: flex-start;
  width: 50%;
}
.parent div:nth-child(3) {
  order: 3;
  align-self: flex-end;
}
```

### التكليف 05

```html
<div class="parent">
  <div class="one">1</div>
  <div class="two">2</div>
  <div class="three">3</div>
  <div class="four">4</div>
</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر parent هو 600px والطول هو 300px
- قم بتوسيط العنصر parent في الصفحة بطريقة عرضية
- قم بعمل نفس العناصر بنفس شكلها وأماكنها

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 10px;
  --red: #f44336;
  --green: #009688;
  --blue: #05a9f4;
  --orange: #ff9800;
  --purple: #673ab7;
  --brown: #795548;
  --light-green: #8ac34a;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.parent {
  width: 600px;
  padding: 10px;
  height: 300px;
  display: flex;
  flex-flow: row;
  justify-content: space-between;
  /* align-content: space-evenly; */
  /* gap: 10px; */
  background-color: var(--white);
}

.parent div {
  padding: 10px;
  width: 100px;
  height: 150px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--white);
  font-size: 1.5rem;
  font-weight: 600;
  background-color: var(--green);
}

.parent .one {
  order: 2;
  background-color: var(--orange);
}
.parent .two {
  order: 3;
  background-color: var(--light-green);
  align-self: flex-end;
}
.parent .three {
  order: 4;
  background-color: var(--brown);
}

.parent .four {
  order: 1;
  background-color: var(--purple);
  align-self: flex-end;
}
```

### التكليف 06

```html
<div class="page">
  <div class="header">
    <div class="logo">Logo</div>
    <ul class="links">
      <li>Home</li>
      <li>About</li>
      <li>Services</li>
      <li>Contact</li>
    </ul>
  </div>
  <div class="main-area">
    <div class="content">Content</div>
    <div class="sidebar">Sidebar</div>
  </div>
  <div class="footer">
    <div class="copyright">Copyright 2021</div>
    <div class="design">Designed By Elzero</div>
  </div>
</div>
```

- يمكنك إستخدام البنية السابقة أو عمل بنية بواسطة ال HTML5 Semantic Elements لتصل لنفس الشكل
- إستعمل ال Flex Box فقط في توزيع العناصر لتقوم بعمل الشكل التالي
- إستخدم خبراتك فيما تعلمته سابقا للوصول لنفس الشكل
- يجب عليك إستخدام المتغيرات ( Variables ) في كل شيء يتكرر في التصميم

```html
<div class="semantic-page flex">
  <header class="header flex">
    <h1 class="logo flex"><span class="left">&lt;</span> Abdallah Sayed <span class="mid">&#47;</span><span class="right">&gt;</span></h1>
    <nav class="navbar flex">
      <ul class="links flex">
        <li>Home</li>
        <li>About</li>
        <li>Services</li>
        <li>Contact</li>
      </ul>
    </nav>
  </header>
  <main class="main-area flex">
    <section class="content">
      <h2 class="section-title">Content</h2>
    </section>
    <aside class="sidebar">
      <h2 class="sidebar-title">Sidebar</h2>
    </aside>
  </main>
  <footer class="footer flex">
    <p class="copyright">&copy; 2021</p>
    <p class="design">Designed By Abdallah Sayed</p>
  </footer>
</div>
```

```css
* {
  padding: 0;
  margin: 0;
  font-size: 1.5rem;
  font-weight: 400;
  color: var(--black);
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 10px;
  --red: #f44336;
  --green: #009688;
  --blue: #05a9f4;
  --orange: #ff9800;
  --purple: #673ab7;
  --brown: #795548;
  --light-green: #8ac34a;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

.flex {
  display: flex;
  justify-content: center;
  align-items: center;
}

.semantic-page {
  width: 100vh;
  max-width: 1200px;
  height: calc(100svh - 40px);
  padding: 10px;
  margin: 20px auto;
  justify-content: space-between;
  gap: 10px;
  flex-flow: column wrap;
  background-color: var(--white);
}

.logo,
.navbar,
.footer {
  height: 50px;
}

.logo,
.navbar,
.content,
.sidebar,
.footer {
  background-color: var(--light-gray);
}

.header {
  width: 100%;
  height: 50px;
  justify-content: space-between;
  gap: 10px;
}

.header .logo {
  flex: 1;
  height: 50px;
  gap: 5px;
}

.header .logo .mid {
  margin-right: -5px;
}

.navbar {
  padding: 0 10px;
  flex: 4;
  justify-content: flex-end;
}

.navbar .links {
  justify-content: flex-end;
  gap: 10px;
}

.navbar .links li {
  list-style: none;
}

.main-area {
  width: 100%;
  flex-grow: 1;
  gap: 10px;
  justify-content: space-between;
}
.content,
.sidebar,
.footer {
  padding: 10px;
}
.content {
  flex: 2;
  height: 100%;
}

.sidebar {
  flex: 1;
  height: 100%;
}

.footer {
  width: 100%;
  justify-content: space-between;
}
```
