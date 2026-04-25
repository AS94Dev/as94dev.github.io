# تكليفات CSS الدروس من 38 إلى 41

## [ 3 ] تكليفات خاصة ب [ Border Radius, Box Shadow ]

### التكليف 01

```html
<div></div>
<div></div>
<div></div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل نفس الشكل
- تأكد أنك تستعمل نفس الألوان الموجودة في الشكل
- طول وعرض العنصر هو 100px
- يجب عليك كتابة ال Prefixes للخواص التي تحتاج ل Prefix

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
  display: inline-block;
  position: relative;
  width: 100px;
  height: 100px;
  margin: 20px;
  margin-right: 0;
  background-color: var(--light-gray);
  border-radius: 50%;
  border: 3px solid var(--black);
  box-shadow:
    3px 3px var(--blue),
    -3px -3px var(--red);
  counter-increment: div 1;
}

div::after {
  content: counter(div);
  position: absolute;
  width: 24px;
  height: 24px;
  background-color: var(--black);
  color: var(--white);
  text-align: center;
  line-height: 24px;
  border-radius: 50%;
  top: -11px;
  left: calc((100% / 2) - 14px);
}
div::before {
  content: "Element";
  position: absolute;
  width: 100%;
  height: 100%;
  line-height: 90px;
  text-align: center;
}
```

### التكليف 02

```html
<div></div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل نفس الشكل
- تأكد أنك تستعمل نفس الألوان الموجودة في الشكل
- طول وعرض العنصر هو 100px
- يجب عليك كتابة ال Prefixes للخواص التي تحتاج ل Prefix
- تأكد ان العنصر موسط في الشاشة طوليا وعرضيا

```css
div {
  width: 100px;
  height: 100px;
  margin: 20px auto;
  background-color: var(--light-gray);
  box-shadow: 0 0 5px inset var(--black);
  border-radius: 10px 50px;
}
```

### التكليف 03

- تأكد أنك تستعمل نفس الألوان الموجودة في الشكل
- العنصر الأب الذي يحمل جميع العناصر عرضه هو 550px
- يجب عليك كتابة ال Prefixes للخواص التي تحتاج ل Prefix
- تأكد ان العنصر موسط في الشاشة عرضيا

```html
<div class="plans">
  <div class="plan basic">
    <h2 class="title">basic</h2>
    <p class="price">free</p>
  </div>
  <span></span>
  <div class="plan pro">
    <h2 class="title">pro</h2>
    <p class="price">$30</p>
  </div>
</div>
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

.plans {
  width: 550px;
  margin: 20px auto;
  overflow: hidden;
  position: relative;
}

.basic,
.pro {
  width: calc((100% - 82px) / 2);
  height: fit-content;
  margin: 20px;
  background-color: var(--light-gray);
  border-radius: 5px;
  float: left;
}

span::before {
  content: "";
  position: absolute;
  width: 2px;
  height: calc(100% - 40px);
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: var(--blue);
  z-index: -1;
}

span::after {
  content: "Or";
  position: absolute;
  width: 25px;
  height: 25px;
  text-align: center;
  line-height: 25px;
  color: var(--white);
  font-size: 0.8rem;
  font-weight: 600;
  border-radius: 50%;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: var(--blue);
}

.title {
  padding: 10px;
  margin: 20px;
  text-align: center;
  color: var(--white);
  font-size: 1rem;
  text-transform: capitalize;
  background-color: var(--blue);
  border-radius: 5px;
  border-radius: 5px;
}

.price {
  width: 150px;
  height: 150px;
  margin: 20px auto;
  text-align: center;
  line-height: 150px;
  border-radius: 50%;
  font-size: 1.5rem;
  text-transform: capitalize;
  background-color: var(--white);
}
```
