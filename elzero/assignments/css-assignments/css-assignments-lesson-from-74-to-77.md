# تكليفات CSS الدروس من 74 إلى 77

## [ 4 ] تكليفات خاصة ب [ Animation ]

### التكليف 01

```html
<div></div>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر وطوله هو 50px
- قم بتوسيط العنصر في الصفحة بطريقة طولية وعرضية
- قم بعمل الشكل بنفس الالوان
- مدة ال Animation هي ثانية واحدة
- عند عمل Hover على العنصر تأكد أن Animation سيتوقف

```css
div {
  width: 50px;
  height: 50px;
  position: relative;
  border-radius: 50%;
  border: 5px solid var(--red);
  border-left-color: transparent;
  animation-name: spin;
  animation-duration: 1s;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  animation-play-state: running;
}

div:hover {
  animation-play-state: paused;
}

div::after,
div::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  translate: -50% -50%;
  border-radius: 50%;
  border: 5px solid;
}

div::after {
  width: 150%;
  height: 150%;
  border-color: var(--blue);
  border-right-color: transparent;
}
div::before {
  width: 200%;
  height: 200%;
  border-color: var(--orange);
  border-left-color: transparent;
  rotate: 90deg;
}

@keyframes spin {
  to {
    rotate: 1turn;
  }
}
```

### التكليف 02

```html
<div></div>
```

- عرض العنصر وطوله هو 50px
- قم بتوسيط العنصر في الصفحة بطريقة طولية وعرضية
- قم بعمل الشكل بنفس الالوان
- مدة ال Animation في أول عنصر الأزرق هو ثانية واحدة
- تأكد أن ال Animation سوف يعمل عند عمل Hover فقط

```css
div {
  width: 50px;
  height: 50px;
  position: relative;
  border-radius: 50%;
  border: 5px solid var(--blue);
  border-bottom-color: transparent;
  animation-name: spin;
  animation-duration: 1s;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  animation-play-state: paused;
}

div::after,
div::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  translate: -50% -50%;
  border-radius: 50%;
  border: 5px solid;
  animation-name: spin;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
  animation-play-state: paused;
}

div::after {
  width: 150%;
  height: 150%;
  border-color: var(--orange);
  border-bottom-color: transparent;
  animation-duration: 2s;
}
div::before {
  width: 200%;
  height: 200%;
  border-color: var(--black);
  border-bottom-color: transparent;
  animation-duration: 3s;
}

div:hover,
div:hover::after,
div:hover::before {
  animation-play-state: running;
}

@keyframes spin {
  to {
    rotate: 1turn;
  }
}
```

### التكليف 03

```html
<span></span>
```

- إستخدم البنية السابقة بدون التعديل عليها لعمل الشكل المطلوب
- عرض العنصر وطوله هو 50px
- قم بتوسيط العنصر في الصفحة بطريقة طولية وعرضية
- قم بعمل الشكل بنفس الالوان
- مدة ال Animation هي ثانية واحدة

```css
span {
  width: 50px;
  height: 50px;
  background-color: var(--light-gray);
  border-radius: 50%;
  border: 5px solid var(--black);
  border-left-color: transparent;
  animation: spin 1s linear 0s infinite reverse forwards;
}

@keyframes spin {
  to {
    rotate: 1turn;
  }
}
```

### التكليف 04

- قم بعمل نفس الشكل بنفس الألوان
- قم بعمل نفس ال Animation ولا تشترط مدة معينة. أهم شيء أن يبدأ ال Animation الثاني بعد إنتهاء الأول
- إستخدم Flex Box أو Grid في رسم الحروف

```html
<div class="container" flex>
  <div class="e">
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
  <div class="l">
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
    <span></span>
  </div>
</div>
```

```css
.container {
  gap: 20px;
}

.e,
.l {
  display: grid;
  grid-template-columns: repeat(3, 25px);
  grid-template-rows: repeat(7, 25px);
}

.e {
  position: relative;
  grid-template-areas: "t t t" "l1 . ." "l2 . ." "m m m" "l3 . ." "l4 . ." "b b b";
}

.l {
  position: relative;
  grid-template-areas: "l . ." "l . ." "l . ." "l . ." "l . ." "l . ." "b b b";
}

.e::after {
  content: "";
  width: 12.5px;
  height: 12.5px;
  position: absolute;
  right: 6.25px;
  top: 6.25px;
  background-color: var(--orange);
  animation-name: e-move;
  animation-duration: 5s;
  animation-timing-function: linear;
  animation-fill-mode: forwards;
}

.l::after {
  content: "";
  width: 12.5px;
  height: 12.5px;
  position: absolute;
  right: 6.25px;
  bottom: 6.25px;
  opacity: 0;
  background-color: var(--orange);
  animation-name: l-move;
  animation-duration: 3s;
  animation-timing-function: linear;
  animation-fill-mode: forwards;
  animation-delay: 5s;
}

.container span {
  background-color: var(--black);
}

.e span:nth-of-type(1),
.e span:nth-of-type(2),
.e span:nth-of-type(3) {
  grid-area: t;
}

.e span:nth-of-type(4) {
  grid-area: l1;
}

.e span:nth-of-type(5) {
  grid-area: l2;
}

.e span:nth-of-type(6),
.e span:nth-of-type(7),
.e span:nth-of-type(8) {
  grid-area: m;
}

.e span:nth-of-type(9) {
  grid-area: l3;
}

.e span:nth-of-type(10) {
  grid-area: l4;
}

.e span:nth-of-type(11),
.e span:nth-of-type(12),
.e span:nth-of-type(13) {
  grid-area: b;
}

.l span:nth-of-type(1),
.l span:nth-of-type(2),
.l span:nth-of-type(3),
.l span:nth-of-type(4),
.l span:nth-of-type(5),
.l span:nth-of-type(6) {
  grid-area: l;
}

.l span:nth-of-type(7),
.l span:nth-of-type(8),
.l span:nth-of-type(9) {
  grid-area: b;
}

@keyframes e-move {
  0% {
    opacity: 1;
  }
  10% {
    transform: translateX(-50px);
    opacity: 1;
  }
  20% {
    transform: translateX(-50px) translateY(75px);
    opacity: 1;
  }
  40% {
    transform: translateY(75px);
    opacity: 1;
  }
  60% {
    transform: translateX(-50px) translateY(75px);
    opacity: 1;
  }
  80% {
    transform: translateX(-50px) translateY(150px);
    opacity: 1;
  }
  100% {
    transform: translateY(150px);
    opacity: 1;
  }
}

@keyframes l-move {
  0% {
    opacity: 1;
  }
  50% {
    transform: translateX(-50px);
    opacity: 1;
  }
  99% {
    transform: translateX(-50px) translateY(-150px);
    opacity: 1;
  }
  100% {
    transform: translateX(-50px) translateY(-150px);
    visibility: hidden;
  }
}
```
