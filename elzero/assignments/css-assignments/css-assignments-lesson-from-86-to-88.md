# تكليفات CSS الدروس من 86 إلى 88

## [ 2 ] تكليفات خاصة ب [ Global Values ]

### التكليف 01

- قم بعمل Framework لنفسك يحتوي على الإمكانيات التالية
  - أولا Class بإسم “center-flex” عند وضعه على عنصر يقوم بتوسيط العناصر التي بداخله بطريقة طولية وعرضية بواسطة ال Flex
  - ثانيا Class بإسم “center-position” عند وضعه على عنصر يقوم بتوسيط العنصر طوليا وعرضيا في العنصر الأب
  - ثالثا Class بإسم “circle-100” عند وضعه على عنصر يقوم بجعل العرض والطول هو 100px ثم يقوم بتحويله إلى دائرة
  - رابعا Class بإسم “circle-200” عند وضعه على عنصر يقوم بجعل العرض والطول هو 200px ثم يقوم بتحويله إلى دائرة

```css
/* Framework */

.center-flex {
  display: flex;
  justify-content: center;
  align-items: center;
}

.center-position {
  position: absolute;
  top: 50%;
  left: 50%;
  translate: -50% -50%;
}

.circle-100 {
  width: 100px;
  height: 100px;
  border-radius: 50%;
}

.circle-200 {
  width: 200px;
  height: 200px;
  border-radius: 50%;
}
```

### التكليف 02

- قم بعمل Class بإسم arrow ومعه Classes تخص جميع الإتجاهات top, right, bottom, left
- تأكد أن كل Class خاص بإتجاه معين يظهر السهم في نفس الإتجاه
- تأكد أن Class الإتجاه لا يعمل إلا في وجود Class المسمى arrow
- تأكد أن السهم دائما في المنتصف بغض النظر عن طول وعرض العنصر

```html
<div class="arrow top">Elzero</div>
<div class="arrow right">Elzero</div>
<div class="arrow bottom">Elzero</div>
<div class="arrow left">Elzero</div>
```

```css
.container {
  flex-flow: column wrap;
  gap: 50px;
}

.container div {
  position: relative;
  width: 400px;
  padding: 15px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 2rem;
  background-color: var(--bg-card);
}

/* arrow */
.container div.arrow::after {
  content: "";
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: var(--bg-card);
  rotate: 45deg;
  z-index: -1;
}

.container div.arrow.top::after {
  top: -10px;
}
.container div.arrow.right::after {
  right: -10px;
}
.container div.arrow.bottom::after {
  bottom: -10px;
}
.container div.arrow.left::after {
  left: -10px;
}

.container div.arrow.top::after,
.container div.arrow.bottom::after {
  left: 50%;
  translate: -50% 0; /* توسيط أفقي */
}

.container div.arrow.right::after,
.container div.arrow.left::after {
  top: 50%;
  translate: 0 -50%; /* توسيط رأسي */
}
```
