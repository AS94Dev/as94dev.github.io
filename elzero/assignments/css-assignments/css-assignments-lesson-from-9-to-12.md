# تكليفات CSS الدروس من 09 إلى 12

## [ 2 ] تكليفات خاصة ب [ Border, Outline, Display ]

### التكليف 01

- قم بعمل ثلاث عناصر نوعهم Div
- قم بوضع الثلاث عناصر بجانب بعضهم وبدون تحديد عرض لهم
- قم بعمل نفس الشكل الموجود في المثال بنفس الألوان
- حجم كل حافة من الحواف هو 5px

```html
<div class="shape shape-1">Shape 1</div>
<div class="shape shape-2">Shape 2</div>
<div class="shape shape-3">Shape 3</div>
```

```css
.shape {
  display: inline-block;
  padding: 30px;
  margin: 10px;
  background-color: #d4d4d4;
  border: 5px solid;
  outline: 5px solid black;
  font-family: sans-serif;
  font-weight: 500;
}

.shape-1 {
  border-color: red;
}
.shape-2 {
  border-color: blue green blue green;
}
.shape-3 {
  border-style: dashed;
  border-color: red green blue yellow;
}
```

## التكليف 02

```html
<div class="element element-1">This Is Important Note</div>
<div class="element element-2">This Is Important Note</div>
<div class="element element-3">This Is Important Note</div>
```

- إستخدم البنية السابقة ولا تقم بالتعديل عليها
- عرض العناصر هو 400px
- العنصر الثاني قم بإخفائه مع الحفاظ على مكانه في مساحة العمل
- قم بعمل الشكل كما في الصورة بنفس الألوان

```css
.element {
  width: 400px;
  padding: 10px;
  margin: 20px;
  background-color: #eeeeee;
  border-left: 5px solid;
  outline: 5px solid #eeeeee;
}

.element-1 {
  border-left-color: #e91d63;
}
.element-2 {
  visibility: hidden;
}
.element-3 {
  border-left-color: #009688;
}
```
