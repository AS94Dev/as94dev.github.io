# تكليفات CSS الدروس من 05 إلى 08

## [ 4 ] تكليفات خاصة ب [ Background, Margin, Padding ]

### التكليف 01

```html
<div class="assign-1-shape-1">Normal Div</div>
<div class="assign-1-shape-2">Normal Div</div>
<div class="assign-1-shape-3">Normal Div</div>
```

- إستخدم البنية السابقة لعمل المطلوب
- ال Div عرضه هو 500px
- قم بتوسيط ال Div داخل الصفحة بطريقة عرضية
- قم بعمل هوامش داخلية قدرها 20px
- قم بعمل خلفية لل Div لونها blueviolet
- قم بتكرار السطر الخاص بالألوان بكل الطرق التالية [ RGB | HSL | Hex ]
- قم بعمل Div آخر تحته بنفس الخلفية ولكن نسبة الشفافية Alpha Channel تكون النصف
- قم بعمل Div آخر تحته بنفس الخلفية ولكن نسبة الشفافية Alpha Channel تكون 1 من 10

```css
div {
  width: 500px;
  padding: 20px;
  margin: 20px auto;
  background-color: blueviolet;
  background-color: rgb(138, 44, 226);
  background-color: hsl(271, 76%, 53%);
  background-color: #8a2be2;
  font-family: sans-serif;
  font-weight: 500;
  color: aliceblue;
}

.assign-1-shape-2 {
  background-color: rgba(138, 44, 226, 0.5);
}

.assign-1-shape-3 {
  background-color: rgba(138, 44, 226, 0.1);
}
```

### التكليف 02

```html
<div class="assign-2-shape-1">Normal Div</div>
<div class="assign-2-shape-2">Normal Div</div>
<div class="assign-2-shape-3">Normal Div</div>
<div class="assign-2-shape-4">Normal Div</div>
```

- إستخدم البنية السابقة لعمل المطلوب
- ال Div طوله وعرضه هو 400px
- قم بوضع الصورة الموجودة في بداية التكليفات خلفية للعنصر
- في Shape 1 قم بجعل الخلفية لا تتكرر نهائيا
- في Shape 2 قم بجعل الخلفية تتكرر طوليا فقط
- في Shape 3 قم بجعل الخلفية تتكرر عرضيا فقط
- في Shape 4 قم بجعل الخلفية تتكرر طوليا وعرضيا

```css
div {
  width: 400px;
  height: 400px;
  margin: 20px auto;
  background-image: url(./images/image.png);
  color: aliceblue;
  font-family: sans-serif;
  font-weight: 500;
  border: 2px solid #111;
}

.assign-2-shape-1 {
  background-repeat: no-repeat;
}
.assign-2-shape-2 {
  background-repeat: repeat-y;
}
.assign-2-shape-3 {
  background-repeat: repeat-x;
}
```

### التكليف 03

```html
<div class="assign-3-shape-1">Normal Div</div>
<div class="assign-3-shape-2">Normal Div</div>
<div class="assign-3-shape-3">Normal Div</div>
<div class="assign-3-shape-4">Normal Div</div>
```

- إستخدم البنية السابقة لعمل المطلوب
- ال Div طوله وعرضه هو 400px
- قم بوضع الصورة الموجودة في بداية التكليفات خلفية للعنصر
- في Shape 1 قم بجعل الخلفية لا تتكرر نهائيا
- في Shape 2 قم بجعل الخلفية تتكرر طوليا فقط ومكانها يكون ناحية اليمين
- في Shape 3 قم بجعل الخلفية تتكرر عرضيا فقط ومكانها يكون ناحية الأسفل
- في Shape 4 قم بجعل الخلفية تتكرر طوليا وعرضيا

```css
div {
  width: 400px;
  margin: 20px auto;
  height: 400px;
  color: aliceblue;
  background-image: url(./images/image.png);
  font-family: sans-serif;
  font-weight: 500;
  border: 2px solid #111;
}

.assign-3-shape-1 {
  background: url(./images/image.png) no-repeat;
}
.assign-3-shape-2 {
  background-repeat: repeat-y;
  background-position: right;
  color: black;
}
.assign-3-shape-3 {
  background-repeat: repeat-x;
  background-position: bottom;
  color: black;
}
```

### التكليف 04

```html
<div class="assign-4-shape-1">Normal Div</div>
<div class="assign-4-shape-2">Normal Div</div>
<div class="assign-4-shape-3">Normal Div</div>
<div class="assign-4-shape-4">Normal Div</div>
```

- إستخدم البنية السابقة لعمل المطلوب
- ال Div طوله وعرضه هو 400px
- قم بوضع الصورة الموجودة في بداية التكليفات خلفية للعنصر
- في Shape 1 قم بجعل الخلفية تملأ 80% من الطول والعرض الخاص بالعنصر
- في Shape 2 قم بعمل الشكل مثل الصورة
- في Shape 3 قم بعمل الشكل مثل الصورة
- في Shape 4 قم بجعل الخلفية تأخذ 50% من طول وعرض العنصر وقم بتغيير مكانها

```css
div {
  width: 400px;
  height: 400px;
  margin: 20px auto;
  background-image: url(./images/image.png);
  color: aliceblue;
  font-family: sans-serif;
  font-weight: 500;
  border: 2px solid #111;
}

.assign-4-shape-1 {
  background-repeat: no-repeat;
  background-size: 80%;
}
.assign-4-shape-2 {
  background-repeat: repeat-y;
  background-position: right;
  background-size: 80%;
  color: black;
}
.assign-4-shape-3 {
  background-repeat: repeat-x;
  background-position: bottom;
  background-size: 80%;
  color: black;
}

.assign-4-shape-4 {
  background-repeat: no-repeat;
  background-position: bottom right;
  background-size: 50%
  color: black;
}
```
