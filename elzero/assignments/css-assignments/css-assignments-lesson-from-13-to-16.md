# تكليفات CSS الدروس من 13 إلى 16

## [ 2 ] تكليفات خاصة ب [ Nesting, Dimensions, Overflow ]

### التكليف 01

```html
<div class="parent">
  <div class="child">This Is Child <span class="title">Title</span></div>
  <span class="title">Child Title</span>
  <p>Paragraph Content</p>
</div>
<div class="title">Section Title</div>
```

- شاهد البنية السابقة في المثال ولا تقم بالتعديل عليها
- قم بتلوين كلمة Title باللون الأحمر
- قم بتلوين جملة Child Title باللون الأزرق
- قم بتلوين جملة Paragraph Content باللون الأخضر
- قم بتلوين جملة Section Title باللون الأخضر
- قم بجمع الألوان المتشابهه مع بعضها

```css
.parent {
  font-family: sans-serif;
  font-weight: 500;
}
.parent .child .title {
  color: red;
}
.parent .title {
  color: blue;
}
.parent p,
.title {
  color: green;
}
```

### التكليف 02

- قم بعمل الشكل الموجود في الصورة كما هو بنفس الألوان
- يجب عدم تغيير ال Display الخاص بالعنصر ويظل نوعه Block كما هو
- يجب أن لا يزيد عرض العنصر عن 400px
- في آخر عنصر سوف تجد الكلمات خرجت من الصندوق وهي الآن ظاهرة, المطلوب إخفاء أي شيء يخرج من الصندوق

```html
<div class="title title">Title One</div>
<div class="title title-2">Title Two With More Words</div>
<div class="title title-3">Title Three With Many Many Many Words</div>
<div class="title title-4">Title Four With Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Many Words</div>
```

```css
.title {
  width: fit-content;
  max-width: 400px;
  height: fit-content;
  max-height: 50px;
  padding: 10px;
  margin: 10px;
  overflow: hidden;
  background-color: #a52a2a;
  color: aliceblue;
  font-family: sans-serif;
  font-weight: 500;
}
```
