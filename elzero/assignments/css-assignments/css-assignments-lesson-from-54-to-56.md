# تكليفات CSS الدروس من 54 إلى 56

## [ 2 ] تكليفات خاصة ب [ Filters, Gradient ]

### التكليف 01

```html
<div>Elzero</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر هو 600px
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بعمل الشكل بنفس الالوان
- يجب عدم إستخدام ال Box Shadow

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

body {
  width: 100%;
  height: 100svh;
}

[as-flex="true"] {
  display: flex;
  justify-content: center;
  align-items: center;
}

div {
  position: relative;
  width: 580px;
  padding: 20px;
  display: block;
  text-align: center;
  background-color: var(--white);
  font-size: 2.5rem;
  font-weight: 600;
  letter-spacing: 0.5rem;
}

div::first-letter {
  color: var(--orange);
}

div::after {
  content: "";
  position: absolute;
  width: calc(100% + 20px);
  height: calc(100% + 20px);
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: linear-gradient(to right, var(--orange) 0 20%, var(--blue) 0 40%, var(--light-green) 0 60%, var(--red) 0 80%, var(--purple) 0 90%);
  z-index: -1;
}
```

### التكليف 02

- لديك ثلاثة حقول إدخال عرض كل واحد فيهم 600px
- قم بعمل الشكل التالي كما هو مع التأكد ان الحقول موسطة في الشاشة بطريقة عرضية
- يجب عليك إستخدام نفس الالوان الموجودة في الشكل كلها
- لاحظ لون مؤشر الكتابة أحمر
- يجب عدم إستخدام ال Box Shadow

```html
  <body as-flex="true">
    <form as-flex="true">
      <div><input type="text" value="Elzero" placeholder="One" autofocus /></div>
      <div><input type="text" placeholder="Two" /></div>
      <div><input type="text" placeholder="Three" /></div>
    </form>
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

body {
  width: 100%;
  height: 100svh;
}

[as-flex="true"] {
  display: flex;
  justify-content: center;
  align-items: center;
}

form {
  padding: 10px;
  flex-flow: column wrap;
  gap: 20px;
}

div {
  position: relative;
}

input {
  width: 600px;
  height: 70px;
  padding: 0 20px;
  border: 0;
  background-color: var(--white);
  caret-color: var(--red);
  font-size: 2rem;
  line-height: 70px;
}

input:focus-visible {
  outline: 0;
}

div::after {
  content: "";
  width: 100%;
  height: 3px;
  position: absolute;
  bottom: -3px;
  left: 0;
  background: linear-gradient(to right, var(--red) 0 50%, var(--green) 0 50%);
  z-index: -1;
}

```
