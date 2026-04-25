# تكليفات CSS الدروس من 34 إلى 37

## [ 4 ] تكليفات خاصة ب [ Pseudo Classes, Pseudo Elements ]

### التكليف 01

```html
<div>One</div>
<div></div>
<div>Three</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل نفس الشكل
- تأكد أنك تستعمل نفس الألوان الموجودة في الشكل
- تأكد ان جميع ال divs موسطة في الصفحة بطريقة عرضية
- عرض ال div هو 300px وطوله هو 60px

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 16px;
  --red: #f44336;
  --blue: #05a9f4;
  --green: #009688;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

div {
  width: 300px;
  margin: 20px auto;
  height: 60px;
  background-color: var(--light-gray);
  text-align: center;
  line-height: 60px;
}

div:nth-child(2) {
  background-color: var(--red);
}
```

### التكليف 02

```html
<div>1 Hello, Welcome To Abdallah Sayed's Space!</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل نفس الشكل
- تأكد أنك تستعمل نفس الألوان الموجودة في الشكل
- تأكد ان ال div موسط في الصفحة

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 16px;
  --red: #f44336;
  --blue: #05a9f4;
  --green: #009688;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

div {
  width: fit-content;
  padding: 20px;
  padding-left: 30px;
  margin: 20px auto;
  position: relative;
  background-color: var(--light-gray);
  text-align: center;
}

div::first-letter {
  float: left;
  padding: 10px;
  margin-left: -40px;
  margin-top: -10px;
  background-color: var(--red);
}
```

### التكليف 03

```html
<p data-person="Osama">This Is Very Very Long Comment Number One</p>
<p data-person="Ahmed">This Is Very Very Long Comment Number Two</p>
<p data-person="Sayed">This Is Very Very Long Comment Number Three</p>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل نفس الشكل
- تأكد أنك تستعمل نفس الألوان الموجودة في الشكل

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 16px;
  --red: #f44336;
  --blue: #05a9f4;
  --green: #009688;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

p {
  width: 400px;
  padding: 10px;
  margin: 20px auto;
  position: relative;
  background-color: var(--light-gray);
  border-left: 4px solid var(--red);
}

p::after {
  content: "";
  position: absolute;
  width: 16px;
  height: 16px;
  top: 11px;
  left: -11px;
  background-color: var(--red);
  transform: rotate(45deg);
  z-index: -1;
}

p::before {
  content: attr(data-person);
  position: absolute;
  top: 0px;
  left: -90px;
  padding: 10px;
  text-align: center;
  background-color: var(--light-gray);
}
```

### التكليف 04

```html
<p>This Is Very Very Long Product Title</p>
<p>This Is Very Very Long Product Title</p>
<p>This Is Very Very Long Product Title</p>
<p>This Is Very Very Long Product Title</p>
<p>This Is Very Very Long Product Title</p>
<p>This Is Very Very Long Product Title</p>
```

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

:root {
  font-family: sans-serif;
  font-weight: 500;
  font-size: 16px;
  --red: #f44336;
  --blue: #05a9f4;
  --green: #009688;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

p {
  width: 400px;
  padding: 10px;
  margin: 20px auto;
  position: relative;
  background-color: var(--light-gray);
  border-right: 4px solid var(--red);
  counter-increment: p 1;
}

p::after {
  content: "";
  position: absolute;
  padding: 19px;
  top: 0;
  left: -38px;
  background-color: var(--red);
  z-index: -1;
}

p::before {
  content: counter(p);
  position: absolute;
  top: 0px;
  left: -34px;
  padding: 10px;
  text-align: center;
  color: var(--white);
  font-weight: 600;
}
```
