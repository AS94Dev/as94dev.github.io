# تكليفات CSS الدروس من 22 إلى 26

## [ 3 ] تكليفات خاصة ب [ Inheritance, Typography ]

### التكليف 01

```html
<div>
  <p>This Is Paragraph</p>
</div>
```

- إستخدم البنية السابقة ولا تقم بالتعديل عليها
- قم بعمل الشكل التالي كما هو
- تأكد أن أي تغيير في ال Padding أو ال Border للعنصر الأب ( Div ) يحدث لنفس العنصر الإبن ( P ) بدون التعديل عليه
- الشكل بالأسفل للتوضيح لو قمنا بتغيير الألوان كيف سيكون الشكل

```css
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
  font-weight: 500;
}

div {
  width: 400px;
  padding: 20px;
  margin: 20px auto;
  border: solid 3px #fe5723;
}

p {
  padding: inherit;
  border: inherit;
  text-align: center;
  background-color: #dddddd;
}
```

### التكليف 02

- قم بعمل الشكل التالي بثلاث خطوط مختلفة
- في الشكل الأول قم بإستعمال الخط Open Sans وتأكد أن وزن الخط هو 300 ويكون الخط مائل
- في الشكل الثاني قم بإستعمال الخط Cairo وتأكد أن وزن الخط هو 700
- في الشكل الثالث قم بإستعمال الخط Jomhuria وتأكد أن وزن الخط هو 400

```html
<div class="box">
  <p class="opensans-font">abdallah sayed</p>
  <p class="cairo-font">abdallah sayed</p>
  <p class="jomhuria-font">abdallah sayed</p>
</div>
```

```css
@import url("https://fonts.googleapis.com/css2?family=Cairo:wght@200..1000&family=Jomhuria&family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap");

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
  font-weight: 500;
}

.box {
  width: 300px;
  padding: 10px;
  margin: 10px auto;
  height: fit-content;
  border: 2px solid royalblue;
}

p {
  padding: inherit;
  border: inherit;
  margin: 10px;
  font-size: 26px;
  text-align: center;
  text-transform: capitalize;
}

.opensans-font {
  font-family: "Open Sans", sans-serif;
  font-weight: 300;
  font-style: italic;
}

.cairo-font {
  font-family: "Cairo", sans-serif;
  font-weight: 700;
}

.jomhuria-font {
  font-family: "Jomhuria", serif;
  font-weight: 400;
}
```

### التكليف 03

- حجم الخط في ال Root Element هو 20px
- قم بإستخدام ال Root Time ( Rem ) في الثلاث عناصر التالية لتخرج بالمقاسات المطلوبة
- مطلوب في العنصر الأول أن يكون حجم الخط 50px بال Rem
- مطلوب في العنصر الثاني أن يكون حجم الخط 40px بال Rem
- مطلوب في العنصر الثالث أن يكون حجم الخط 30px بال Rem

```html
<div class="box">
  <p class="text text-1">abdallah sayed</p>
  <p class="text text-2">abdallah sayed</p>
  <p class="text text-3">abdallah sayed</p>
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
  font-size: 20px;
}

.box {
  width: 500px;
  padding: 20px;
  margin: 20px auto;
}

.text {
  padding: inherit;
  text-transform: capitalize;
  text-align: center;
}

.text-1 {
  font-size: 2.5rem;
}
.text-2 {
  font-size: 2rem;
}
.text-3 {
  font-size: 1.5rem;
}
```
