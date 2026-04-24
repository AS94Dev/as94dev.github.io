# تكليفات CSS الدروس من 68 إلى 73

## [ 5 ] تكليفات خاصة ب [ Skew, Matrix, 3D Transform ]

### التكليف 01

```html
<h1>Elzero</h1>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر هو 150px
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بعمل الشكل بنفس الالوان
- إستخدم المتغيرات في تحديد اللون الأساسي

```css
h1 {
  width: 150px;
  padding: 10px;
  position: relative;
  font-size: 3rem;
  font-weight: 600;
  color: var(--white);
  background-color: var(--orange);
}

h1::after,
h1::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  right: 0;
  background-color: var(--orange);
  z-index: -1;
}

h1::after {
  transform: skewY(10deg);
}
h1::before {
  transform: skewY(-10deg);
}
```

### التكليف 02

```html
<h1>Elzero</h1>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- قم بتوسيط العنصر في الصفحة بطريقة عرضية
- قم بعمل الشكل بنفس الالوان
- إستخدم المتغيرات في تحديد اللون الأساسي

```css
h1 {
  width: 150px;
  padding: 10px;
  position: relative;
  font-size: 3rem;
  font-weight: 600;
  color: var(--white);
  background-color: var(--green);
}

h1::after,
h1::before {
  content: "";
  position: absolute;
  width: 50%;
  height: 100%;
  top: 0;
  left: -10px;
  background-color: var(--green);
}

h1::after {
  width: 5px;
  left: 2px;
  transform: skewX(20deg);
  background-color: var(--white);
}

h1::before {
  transform: skewX(20deg);
  z-index: -1;
}
```

### التكليف 03

```css
.class {
  matrix(3, 0.2679, 0, 3, 20, 100);
}
```

- داخل تعليق قم بكتابة قيم ال Transform كاملة من الكود السابق

```css
/* transform: scaleX(3) skewY(15deg) skewX(0) scaleY(3) translateX(20) translateY(100); */
```

### التكليف 04

```html
<div></div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر وطوله هو 200px
- قم بتوسيط العنصر في الصفحة بطريقة طولية وعرضية
- قم بعمل الشكل بنفس الالوان

```css
div {
  width: 200px;
  padding: 10px;
  height: 200px;
  position: relative;
  border-bottom: 5px solid var(--black);
  background-color: var(--darlington);
}

div::after {
  content: "Elzero";
  position: absolute;
  bottom: 7px;
  left: 10px;
  color: var(--white);
  font-size: 1.8rem;
}

div::before {
  content: "";
  position: absolute;
  width: 200px;
  height: 200px;
  top: calc(-50% - 5px);
  left: -5px;
  translate: (50%);
  rotate: 45deg;
  scale: 0.68;
  border: 5px solid;
  border-color: transparent var(--white) var(--white) transparent;
  background-color: var(--black);
}
```

### التكليف 05

```html
<div></div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر وطوله هو 200px
- قم بتوسيط العنصر في الصفحة بطريقة طولية وعرضية
- قم بعمل الشكل بنفس الالوان
- قم بعمل الشكل مرة بطريقة عرضية ومرة بطريقة طولية

```css
div {
  width: 200px;
  height: 200px;
  background-color: var(--blue);
  transform-origin: center bottom;
  transition: transform 0.7s;
}

div::before {
  content: "Front";
  color: var(--white);
  font-size: 3rem;
  transition: transform 0.7s;
}

div:hover {
  transform: rotate3d(0, 1, 0, 0.5turn);
  background-color: var(--red);
}

div:hover::before {
  content: "Back";
  transform: rotate3d(0, 1, 0, 0.5turn);
}
```

```css
div {
  width: 200px;
  height: 200px;
  background-color: var(--blue);
  /* transform-origin: center bottom; */
  transition: transform 0.7s;
}

div::before {
  content: "Front";
  color: var(--white);
  font-size: 3rem;
  transition: transform 0.7s;
}

div:hover {
  transform: rotate3d(1, 0, 0, 0.5turn);
  background-color: var(--red);
}

div:hover::before {
  content: "Back";
  transform: rotate3d(1, 0, 0, 0.5turn);
}
```
