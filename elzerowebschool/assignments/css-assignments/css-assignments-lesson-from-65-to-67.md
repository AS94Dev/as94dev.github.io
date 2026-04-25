# تكليفات CSS الدروس من 65 إلى 67

## [ 3 ] تكليفات خاصة ب [ Scale, Rotate, Translate ]

### التكليف 01

```html
<div>Elzero</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر هو 300px وطوله هو 200px
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بعمل الشكل بنفس الالوان
- يمكنك توسيط النص داخل العنصر باي طريقة تعجبك

```css
div {
  width: 300px;
  height: 200px;
  position: relative;
  font-size: 4rem;
  font-weight: 600;
  color: var(--blue);
  border: 2px solid var(--light-gray);
  background-color: var(--white);
}

div::after,
div::before {
  content: "";
  width: inherit;
  height: inherit;
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}

div::after {
  transform: rotate(7deg);
  background-color: var(--blue);
}

div::before {
  transform: rotate(-7deg);
  background-color: var(--red);
}
```

### التكليف 02 / التكليف 03

```html
<div>Elzero</div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- طول العنصر وعرضه هو 200px
- قم بتوسيط العنصر في الصفحة بطريقة طولية وعرضية بدون إستخدام
- قم بعمل الشكل بنفس الالوان
- يمكنك توسيط النص داخل العنصر باي طريقة تعجبك

- قم بإستخدام نفس الشكل من التكليف السابق
- عند عمل Hover على الشكل قم بعمل المطلوب في الصورة
- مدة دوران العنصر حول الشكل نصف ثانية

```css
div {
  width: 200px;
  height: 200px;
  position: absolute;
  top: 50%;
  left: 50%;
  translate: -50% -50%;
  border-radius: 50%;
  font-size: 3rem;
  font-weight: 600;
  background-color: var(--light-gray);
  transition: 0.5s ease rotate;
}

div::after,
div::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  translate: -50% -50%;
  border-radius: 50%;
  border: 10px solid;
}

div::after {
  width: calc(100% + 20px);
  height: calc(100% + 20px);
  border-color: var(--blue) transparent var(--blue) var(--blue);
  transition: 0.5s 0.5s ease rotate;
}
div::before {
  width: 100%;
  height: 100%;
  border-color: var(--red) var(--red) var(--red) #fff;
  transition: 0.5s ease rotate;
}

div:hover::before {
  rotate: 1turn 0 0;
}

div:hover::after {
  rotate: 1turn 0 0;
}
```
