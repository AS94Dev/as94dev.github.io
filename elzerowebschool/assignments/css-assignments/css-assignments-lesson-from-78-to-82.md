# تكليفات CSS الدروس من 78 إلى 82

## [ 8 ] تكليفات خاصة ب [ Selectors ]

## المطلوب في التكليفات من 1 لـ 8

- إستخدم البنية السابقة بدون التعديل عليها
- المطلوب تلوين كلمة Elzero باللون الأحمر
- يجب إختيار ال Selector/s بسطر واحد فقط

### التكليف 01

```html
<div class="main red">Elzero</div>
<div class="main">Testing</div>
<div class="red">Testing</div>
<div class="main red">Elzero</div>
<p class="main red">Testing</p>
```

```css
div.main.red {
  font-weight: 600;
  color: red;
}
```

### التكليف 02

```html
<div class="parent">
  <div class="child">Testing</div>
  <div class="child">Elzero</div>
</div>
<div class="parent">
  <div>
    <div class="child">Testing</div>
  </div>
</div>
<div class="child">Testing</div>
```

```css
.parent .child:nth-of-type(2) {
  font-weight: 600;
  color: red;
}
```

### التكليف 03

```html
<div class="parent">
  <div class="baby">Testing</div>
  <div class="baby">Testing</div>
</div>
<div class="parent">
  <div class="baby">Elzero</div>
</div>
<div class="parent">
  <div>
    <div>Testing</div>
  </div>
  <div class="baby">Testing</div>
</div>
<div class="baby">Testing</div>
```

```css
.parent:nth-of-type(2) .baby {
  font-weight: 600;
  color: red;
}
```

### التكليف 04

```html
<p>Testing</p>
<div>Testing</div>
<div>Testing</div>
<div title="Elzero">Elzero</div>
<div title="Hello">Elzero</div>
<div title="HTML">Elzero</div>
<div>Testing</div>
<div class="no-need" title="Elzero">Testing</div>
<div class="parent">
  <div>Testing</div>
  <p>Testing</p>
  <div>Testing</div>
  <div title="Elzero">Testing</div>
  <div>Testing</div>
  <div title="Elzero">Testing</div>
</div>
```

```css
div[title]:is([title="Elzero"], [title="Hello"], [title="HTML"]):not(div.no-need, div.parent div) {
  color: red;
}
```

### التكليف 05

```html
<div>
  <p>Testing</p>
  <div title="Elzero">Testing</div>
  <p>Testing</p>
</div>
<div>
  <p>Testing</p>
  <div title="Elzero">Elzero</div>
</div>
<div class="no-need">
  <p>Testing</p>
  <div title="Elzero">Testing</div>
</div>
<div>
  <p>Testing</p>
  <p>Testing</p>
  <div class="no-need" title="Elzero">Testing</div>
</div>
<div>
  <p title="Elzero">Testing</p>
  <p title="Elzero">Testing</p>
  <div>Testing</div>
</div>
<div>
  <p>Testing</p>
  <div>Testing</div>
  <div>Testing</div>
</div>
```

```css
div:nth-child(2) div[title="Elzero"] {
  color: red;
}
```

### التكليف 06

```html
<div>
  <div>Testing</div>
  <div>Testing</div>
  <div>Elzero</div>
  <div>Testing</div>
</div>
<div>
  <div>Testing</div>
  <div>Testing</div>
  <div>Testing</div>
  <div>Elzero</div>
  <div>Testing</div>
  <p>Testing</p>
</div>
<div class="no-need">
  <div>Testing</div>
  <div>Testing</div>
  <div>Testing</div>
  <div>Testing</div>
</div>
```

```css
div:is(div:nth-of-type(1) div:nth-child(3), div:nth-of-type(2) div:nth-child(4)) {
  color: red;
}
```

### التكليف 07

```html
<div>
  <h3>Testing</h3>
  <div>Testing</div>
  <h3>Testing</h3>
  <h3>Testing</h3>
  <div>Elzero</div>
  <div>Testing</div>
</div>
<div>
  <h3>Testing</h3>
  <div>Testing</div>
  <h3>Testing</h3>
  <p>Testing</p>
  <div>Testing</div>
  <div>Testing</div>
</div>
<div>
  <div>Testing</div>
  <h3>Testing</h3>
  <div>Testing</div>
  <h3>Testing</h3>
  <div class="no-need">Testing</div>
  <div>Testing</div>
  <div>Testing</div>
</div>
<div class="no-need">
  <h3>Testing</h3>
  <div>Testing</div>
  <h3>Testing</h3>
  <div>Testing</div>
  <div>Testing</div>
</div>
<div class="no-need-2">
  <h3>Testing</h3>
  <div>Testing</div>
  <h3>Testing</h3>
  <div>Testing</div>
  <div>Testing</div>
</div>
```

```css
div h3 + div + h3 + h3 + div {
  color: red;
}
```

### التكليف 08

- المطلوب إستخدام :not Selector فقط بجانب نفس الشروط السابقة

```html
<div>
  <div>Testing</div>
  <div>Elzero</div>
  <div>Elzero</div>
  <h3>Testing</h3>
  <p>Elzero</p>
  <h3>Testing</h3>
  <div>Testing</div>
</div>
```

```css
div *:not(h3, div) {
  color: red;
}
```
