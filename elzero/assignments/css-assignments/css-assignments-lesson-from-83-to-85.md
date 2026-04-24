# تكليفات CSS الدروس من 83 إلى 85

## [ 3 ] تكليفات خاصة ب [ Media Queries ]

### التكليف 01

```html
<div class="assign-one">Elzero Web School</div>
```

- قم بتعديل حجم الخط ليكون 40px فقط في حالة ال Print

```css
@media print {
  .assign-one {
    font-size: 40px;
  }
}
```

### التكليف 02

- قم بعمل نفس الشكل
- قم بتوزيع العناصر بنفس العدد في كل شاشة
- يجب التأكد أنك تظهر الالوان في كل شاشة كما في الصور
- يجب إستعمال ال Media Queries فقط ولا تقم بإضافة أي اطار عمل

```html
<div class="container flex">
  <div class="card flex">
    <h2>product 01</h2>
    <p>this is product</p>
  </div>
  <div class="card flex">
    <h2>product 02</h2>
    <p>this is product</p>
  </div>
  <div class="card flex">
    <h2>product 03</h2>
    <p>this is product</p>
  </div>
  <div class="card flex">
    <h2>product 04</h2>
    <p>this is product</p>
  </div>
</div>
```

```css
.container {
  padding: 10px;
  flex-wrap: wrap;
  gap: 10px;
}

.card {
  width: 100%;
  flex-flow: column wrap;
  text-transform: capitalize;
}

.card h2 {
  font-size: 2.5rem;
  font-weight: 700;
}

.card p {
  font-size: 1.5rem;
}

/* Print */
@media print {
}

/* Mobile */
@media (max-width: 767px) {
  .card {
    width: 100%;
  }
}

/* Small */
@media (min-width: 768px) {
}

/* Medium */
@media (min-width: 992px) {
  .card {
    width: calc(50% - 10px);
  }
  .card h2 {
    color: var(--color-danger);
  }
}

/* Large */
@media (min-width: 1200px) {
  .card {
    width: calc(25% - 10px);
  }
  .card h2 {
    color: var(--color-primary);
  }
}
```

### التكليف 03

- قم بعمل نفس الشكل
- قم بتوزيع العناصر بنفس العدد في كل شاشة
- يجب التأكد أنك تظهر الالوان في كل شاشة كما في الصور
- يجب إستعمال ال Media Queries فقط ولا تقم بإضافة أي اطار عمل

```html
<div class="container flex">
  <div class="card flex">
    <h2>product 01</h2>
    <p>this is product</p>
  </div>
  <div class="card flex">
    <h2>product 02</h2>
    <p>this is product</p>
  </div>
  <div class="card flex">
    <h2>product 03</h2>
    <p>this is product</p>
  </div>
  <div class="card flex">
    <h2>product 04</h2>
    <p>this is product</p>
  </div>
</div>
```

```css
.container {
  display: grid;
  gap: 10px;
}

.card {
  width: 100%;
  flex-flow: column wrap;
  text-transform: capitalize;
}

.card h2 {
  font-size: 2.5rem;
  font-weight: 700;
}

.card p {
  font-size: 1.5rem;
}

/* Print */
@media print {
}

/* Mobile */
@media (max-width: 767px) {
}

/* Small */
@media (min-width: 768px) {
}

/* Medium */
@media (min-width: 992px) {
  .container {
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, auto);
  }

  .card:first-of-type {
    grid-column: 1 / span 3;
  }
  .card h2 {
    color: var(--color-danger);
  }
}

/* Large */
@media (min-width: 1200px) {
  .container {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, auto);
  }

  .card:first-of-type {
    grid-column: 1 / span 2;
  }

  .card:last-of-type {
    grid-column: 1 / span 2;
  }
  .card h2 {
    color: var(--color-primary);
  }
}
```
