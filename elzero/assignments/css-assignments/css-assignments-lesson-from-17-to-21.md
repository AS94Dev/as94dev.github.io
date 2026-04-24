# تكليفات CSS الدروس من 17 إلى 21

## [ 4 ] تكليفات خاصة ب [ Text Formatting ]

### التكليف 01

- قم بعمل نفس الشكل التالي
- يجب عليك عمل نفس الألوان

```html
<h1 class="my-name">Abdallah Sayed</h1>
```

```css
.my-name {
  font-family: sans-serif;
  font-weight: 600;
  text-shadow:
    1px 1px 0 #f34336,
    2px 2px 0 #2296f2,
    3px 3px 0 #c06dcb;
}
```

### التكليف 02

```html
<p class="one">elzero Web school</p>
<p class="two">elzero Web school</p>
<p class="three">elzero Web school</p>
```

- إستخدم البنية السابقة ولا تقم بالتعديل عليها
- بواسطة ال CSS قم بعمل الشكل التالي وتأكد أن الحروف تظهر كما في الصورة

```css
p {
  font-family: sans-serif;
  font-weight: 500;
}
.one {
  text-transform: uppercase;
}
.two {
  text-transform: capitalize;
}
.three {
  text-transform: lowercase;
}
```

### التكليف 03

```html
<div>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea itaque fugit vitae incidunt quis dolores? Id alias eveniet sequi perspiciatis iusto impedit, accusamus maxime reprehenderit blanditiis adipisci sapiente hic velit.</div>
```

- إستخدم البنية السابقة ولا تقم بالتعديل عليها
- تأكد أن العنصر له نفس الألوان والهوامش الداخلية وعرض العنصر يكون 400px
- الشكل الأول في الصورة هو الوضع الطبيعي للعنصر. عندما يزيد النص سينزل للسطر التالي
- الشكل الثاني في الصورة المحتوى صغير ولم يصل لنهاية العنصر
- الشكل الثالث النصوص الموجودة فيه هي نفس الموجودة في الشكل الأول
- المطلوب قطع النص عند نهاية العنصر ولا تجعله ينزل للسطر التالي
- الثلاث نقاط يتم وضعها تلقائيا ولا تقم بكتابتها

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.box {
  width: fit-content;
  max-width: 400px;
  padding: 20px;
  margin: 20px;
  background-color: #eeeeee;
  font-family: sans-serif;
  font-weight: 500;
}
.box-2 {
  width: 400px;
}
.box-3 {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
```

### التكليف 04

```html
<a class="my-site" href="https://abdsy.ddns.net">abdallah sayed</a>
```

- إستخدم البنية السابقة ولا تقم بالتعديل عليها
- تأكد ان الرابط سيظهر في منتصف الصفحة تماما
- قم بعمل نفس الألوان وكل شيء ليظهر الشكل كما في المثال

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.my-site {
  display: block;
  width: fit-content;
  height: fit-content;
  padding: 7px 10px 5px 10px;
  margin: 20px auto;
  background-color: #009688;
  border-bottom: 3px solid #00514a;
  font-family: sans-serif;
  color: #ffffff;
  text-decoration: none;
  text-transform: capitalize;
}
```
