# تكليفات CSS الدروس من 57 إلى 64

## [ 6 ] تكليفات خاصة ب [ Grid ]

### التكليف 01

```html
<div class="grid">
  <div></div>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
</div>
```

```css
.grid {
  background-color: #ddd;
  padding: 20px;
  width: 800px;
  height: 400px;
}
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- تنسيقات ال CSS لتوضيح أبعاد العنصر الأب
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بعمل الشكل بنفس الالوان
- إستخدم ال Grid لعمل الشكل الأساسي
- يمكنك توسيط النص داخل العنصر باي طريقة تعجبك
- يجب كتابة الكلمات الموجودة داخل العنصر بواسطة ال CSS

```html
<div class="grid">
  <div as-flex="true"></div>
  <div as-flex="true"></div>
  <div as-flex="true"></div>
  <div as-flex="true"></div>
  <div as-flex="true"></div>
  <div as-flex="true"></div>
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
  --darlington: #5f7d8c;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
}

[as-flex="true"] {
  display: flex;
  justify-content: center;
  align-items: center;
}

.grid {
  width: 800px;
  padding: 20px;
  height: 400px;
  display: grid;
  grid-template: auto 1fr / repeat(3, 1fr);
  gap: 20px;
  background-color: var(--white);
}

.grid div {
  padding: 10px;
  background-color: var(--darlington);
  color: var(--white);
  text-transform: capitalize;
  font-weight: 600;
  counter-increment: div 1;
}

.grid div::after {
  content: "element 0" counter(div);
}
```

### التكليف 02

```html
<div class="layout">
  <header></header>
  <section></section>
  <aside></aside>
  <footer></footer>
</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- قم بعمل الشكل بنفس الالوان
- إستخدم ال Grid لعمل الشكل الأساسي
- يجب كتابة الكلمات الموجودة داخل العنصر بواسطة ال CSS
- يجب عليك أن تملا الصفحة بالتصميم ليكون Full Screen

```html
<div class="layout">
  <header flex padding-10></header>
  <section padding-10></section>
  <aside padding-10></aside>
  <footer flex padding-10></footer>
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
  --darlington: #5f7d8c;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
}

[flex] {
  display: flex;
  justify-content: center;
  align-items: center;
}

[padding-10] {
  padding: 10px;
}

.layout {
  width: 100%;
  height: 100svh;
  display: grid;
  grid-template-rows: 50px 1fr 50px;
  grid-template-areas: "head head head head head head head head head head" "sect sect sect sect sect sect sect side side side" "foot foot foot foot foot foot foot foot foot foot";
}
header,
section,
aside,
footer {
  justify-content: flex-start !important;
  color: var(--white);
  text-transform: capitalize;
}

header {
  grid-area: head;
  background-color: var(--blue);
}

header::after {
  content: "header";
}

section {
  grid-area: sect;
  background-color: var(--orange);
}

section::after {
  content: "section";
}

aside {
  grid-area: side;
  background-color: var(--darlington);
}

aside::after {
  content: "aside";
}

footer {
  grid-area: foot;
  background-color: var(--green);
}

footer::after {
  content: "footer";
}
```

### التكليف 03

```html
<div class="grid">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
  <div>5</div>
  <div>6</div>
  <div>7</div>
  <div>8</div>
</div>
```

```css
.grid {
  background-color: #ddd;
  padding: 20px;
  width: 800px;
  height: 400px;
}
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- تنسيقات ال CSS لتوضيح أبعاد العنصر الأب
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بعمل الشكل بنفس الالوان
- إستخدم ال Grid لعمل الشكل الأساسي

```html
<div class="grid">
  <div flex>1</div>
  <div flex>2</div>
  <div flex>3</div>
  <div flex>4</div>
  <div flex>5</div>
  <div flex>6</div>
  <div flex>7</div>
  <div flex>8</div>
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
  --darlington: #5f7d8c;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
}

[flex] {
  display: flex;
  justify-content: center;
  align-items: center;
}

[p10] {
  padding: 10px;
}

[p20] {
  padding: 20px;
}

[m20] {
  margin: 20px;
}

.grid {
  width: 800px;
  padding: 20px;
  height: 400px;
  display: grid;
  grid-template: 1fr auto / auto 1fr 1fr auto;
  gap: 20px;
  background-color: var(--white);
}

div {
  font-weight: 600;
  color: var(--white);
  background-color: var(--black);
}
```

### التكليف 04

```html
<div class="grid">
  <div class="one">1</div>
  <div class="two">2</div>
  <div class="three">3</div>
  <div class="four">4</div>
  <div class="five">5</div>
  <div class="six">6</div>
  <div class="seven">7</div>
  <div class="eight">8</div>
</div>
```

```css
.grid {
  background-color: #ddd;
  padding: 20px;
  width: 800px;
  height: 400px;
}
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- تنسيقات ال CSS لتوضيح أبعاد العنصر الأب
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بعمل الشكل بنفس الالوان
- إستخدم ال Grid لعمل الشكل الأساسي

```html
<div class="grid">
  <div class="one" flex>1</div>
  <div class="two" flex>2</div>
  <div class="three" flex>3</div>
  <div class="four" flex>4</div>
  <div class="five" flex>5</div>
  <div class="six" flex>6</div>
  <div class="seven" flex>7</div>
  <div class="eight" flex>8</div>
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
  --darlington: #5f7d8c;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
}

[flex] {
  display: flex;
  justify-content: center;
  align-items: center;
}

[p10] {
  padding: 10px;
}

[p20] {
  padding: 20px;
}

[m20] {
  margin: 20px;
}

.grid {
  width: 800px;
  padding: 20px;
  height: 400px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(6, 1fr);
  gap: 20px;
  background-color: var(--white);
}

div {
  font-weight: 600;
  color: var(--white);
  background-color: var(--blue);
}

.one {
  grid-area: 6 / span 4;
}

.two {
  grid-area: 2 / span 3;
}

.four {
  grid-area: 3;
}

.five {
  grid-area: 3 / span 3 / span 3;
}

.eight {
  grid-area: 1 / span 4;
}
```

### التكليف 05

```html
<div class="grid">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>
```

```css
.grid {
  background-color: #ddd;
  padding: 20px;
  width: 800px;
  height: 400px;
}
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- تنسيقات ال CSS لتوضيح أبعاد العنصر الأب
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بعمل الشكل بنفس الالوان
- إستخدم ال Grid لعمل الشكل الأساسي

```html
<div class="grid">
  <div flex>1</div>
  <div flex>2</div>
  <div flex>3</div>
  <div flex>4</div>
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
  --darlington: #5f7d8c;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  width: 100%;
  height: 100svh;
}

[flex] {
  display: flex;
  justify-content: center;
  align-items: center;
}

[p10] {
  padding: 10px;
}

[p20] {
  padding: 20px;
}

[m20] {
  margin: 20px;
}

.grid {
  width: 800px;
  padding: 20px;
  height: 400px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-content: space-between;
  gap: 20px;
  background-color: var(--white);
}

div {
  font-weight: 600;
  color: var(--white);
  background-color: var(--blue);
}
```

### التكليف 06

- عمل نفس الشكل مع إمكانية وضع أي بيانات تريدها
- يجب عليك عمل نفس الالوان
- يجب عليك إستخدام ال CSS Grid فقط في توزيع العناصر
- يجب عدم إستخدام ال Margin نهائيا بين العناصر
- يجب عدم إستخدام خواص العرض والطول نهائيا [ Width, Height, Flex-Basis ]

```html
<main class="co-team-grid">
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Osama Mohamed</h2>
      <p class="job-title">Full-Stack Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente!</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Ahmed Sayed</h2>
      <p class="job-title">IOS Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Shady Nabil</h2>
      <p class="job-title">Full-Stack Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente! Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente! Lorem ipsum dolor sit amet consectetur adipisicing elit. Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Mohamed Ibrahim</h2>
      <p class="job-title">.Net Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente!</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Mahmoud Mohamed</h2>
      <p class="job-title">Full-Stack Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente!</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Ezz Eldin</h2>
      <p class="job-title">Front-End Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed illo, quisquam eaque numquam explicabo perspiciatis. Quo earum repellendus officia nesciunt itaque quidem quod, fuga quae, tenetur, voluptates beatae placeat sapiente!</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Mohamed Sayed</h2>
      <p class="job-title">IOS Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Ibrahim Sayed</h2>
      <p class="job-title">IOS Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Gamal Sayed</h2>
      <p class="job-title">IOS Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </article>
  <!--  -->
  <!--  -->
  <article class="post">
    <div class="dev-info">
      <h2 class="name">Eman Sayed</h2>
      <p class="job-title">IOS Developer</p>
    </div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
  </article>
  <!--  -->
</main>
```

```css
* {
  padding: 0;
  margin: 0;
  font-size: 1.5rem;
  font-weight: 400;
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
  --darlington: #5f7d8c;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

body {
  padding: 50px;
  background-color: var(--light-gray);
}

.co-team-grid {
  display: grid;
  grid-template-columns: repeat(4, minmax(200px, 200px));
  gap: 10px;
}

.post {
  padding: 10px;
  display: grid;
  align-content: flex-start;
  gap: 20px;
  border-bottom: 2px solid var(--red);
  background-color: var(--white);
}

.name {
  font-weight: bold;
}

.job-title {
  color: var(--darlington);
  font-weight: bold;
  font-size: 1.1rem;
}

.post p:nth-of-type(1) {
  font-weight: bold;
}

.post:nth-child(1) {
  grid-column: span 2;
}

.post:nth-child(3) {
  grid-row: span 4;
  color: var(--white);
  background-color: var(--black);
}

.post:nth-child(4) {
  grid-row: span 3;
}

.post:nth-child(5) {
  grid-column: span 2;
  grid-row: span 2;
  color: var(--white);
  background-color: var(--black);
}
.post:nth-child(6) {
  grid-column: span 2;
}
.post:nth-child(8) {
  color: var(--white);
  background-color: var(--black);
}
```
