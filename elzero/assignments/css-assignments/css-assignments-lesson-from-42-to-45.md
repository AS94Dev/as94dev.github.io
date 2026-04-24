# تكليفات CSS الدروس من 42 إلى 45

## [ 3 ] تكليفات خاصة ب [ Transitions, Variables ]

### التكليف 01

- تأكد أنك تستعمل نفس الألوان الموجودة في الشكل
- يجب عليك كتابة ال Prefixes للخواص التي تحتاج ل Prefix
- تأكد أن العنصر الأب يذهب للأعلى في نصف ثانية عند ال Hover
- تأكد أن العنصر الأبن يذهب للأسفل بعد الإنتظار نصف ثانية

```html
<div class="parent">
  will go up on hover in 0.5s
  <div class="child">will go down after 0.5s</div>
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

.parent {
  width: 300px;
  height: 150px;
  padding: 10px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: var(--white);
  transition: 0.5s linear top;
  text-align: center;
}

.parent:hover {
  top: 40%;
}

.child {
  padding: 10px;
  transform: translate(0, 10px);
  background-color: var(--light-gray);
  transition: margin 0.5s linear 0.5s;
}

.parent:hover .child {
  margin-top: 10px;
}
```

### التكليف 02

```html
<div
  style="
  background-color: red;
  color: white;
  padding: 20px;
  border: 1px solid blue;
  font-size: 80px;"
>
  Hello Div
</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل نفس الشكل
- تأكد أنك تستعمل نفس الألوان الموجودة في الشكل
- لديك الحرية في عمل ما تريد في ال CSS
- تأكد أن جملة Hello Div تغيرت إلى Elzero
- عرض العنصر هو 400px وهو موسط بطريقة عرضية
- حجم الخط هو 20px

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
  --blue: #05a9f4;
  --green: #009688;
  --black: #333333;
  --white: #f4f4f4;
  --light-gray: #dbdbdb;
}

div {
  width: 100%;
  max-width: 400px;
  height: 60px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: var(--light-gray) !important;
  font-size: 0rem !important;
  border: none !important;
}

div::after {
  content: "Elzero";
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  text-align: center;
  line-height: 60px;
  color: var(--black);
  font-size: 2rem;
  font-weight: 600;
}
```

### التكليف 03

```html
<div>Element</div>
<div>Element</div>
<div>Element</div>
```

```css
:root {
  --mainColor: #009688;
  --mainPadding: 10px;
}

div {
  ???
}
```

- إستخدم بنية ال HTML السابقة بدون التعديل عليها لعمل الشكل التالي
- في ال CSS لا تقم بالتعديل على جزء المتغيرات أبدا وقم بالتعديل على ال div Selector فقط
- تأكد أنك تستخدم المتغيرات لأننا سنقوم بإزالتها لاحقا
- بعد الإنتهاء تماما سنقوم بعمل بعض التعديلات للتأكد أنك قمت بعمل Fall Back لقيم المتغير
- قم بعمل إلغاء للعنصر :root مع المتغيرات داخله
- تأكد أن الشكل سيكون كما في الصورة التالية

```css
:root {
  /* --mainColor: #009688; */
  /* --mainPadding: 10px; */
}

div {
  width: 400px;
  padding: var(--mainPadding, 10px);
  margin: 10px auto;
  border: 3px solid var(--mainColor, black);
  font-family: sans-serif;
  font-weight: 500;
  color: var(--mainColor, red);
}
```
