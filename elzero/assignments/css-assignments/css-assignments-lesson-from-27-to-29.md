# تكليفات CSS الدروس من 27 إلى 29

## [ 2 ] تكليفات خاصة ب [ Float, Opacity ]

### التكليف 01

- قم بعمل الشكل التالي مع مراعاة المعلومات التالية
- العنصر الأب الذي يحتوي على جميع العناصر الداخلية عرضه 800px
- العنصر الأب لا يوجد فيه Padding
- المسافات بين العناصر الداخلية من اليمين واليسار ( Gap ) قدرها 15px
- المسافات بين العناصر الداخلية من الأسفل والأعلى قدرها 15px
- يجب ألا تحسب عرض العنصر بنفسك ويجب أن يكون Dynamic لأننا سنقوم بتغيير عرض العنصر الأب
- قم بتغيير عرض العنصر الأب إلى 1000px وتأكد أنه لم يخرب أي شيء

```html
<div class="father">
  <div class="child child-full">Full Width</div>
  <div class="child child-third">1/3</div>
  <div class="child child-third">1/3</div>
  <div class="child child-third">1/3</div>
  <div class="child child-half">1/2</div>
  <div class="child child-half">1/2</div>
  <div class="child child-quarter">1/4</div>
  <div class="child child-quarter">1/4</div>
  <div class="child child-quarter">1/4</div>
  <div class="child child-quarter">1/4</div>
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

.father {
  width: 1000px;
  margin: 20px auto;
  overflow: hidden;
  border-radius: 5px;
  background-color: #eee;
}

.child {
  float: left;
  padding: 15px;
  margin: 15px 0 0 15px;
  background-color: #ddd;
  text-align: center;
  border-radius: 5px;
}

.child-full {
  width: calc(100% - 30px);
}

.child-third {
  width: calc((100% - 60px) / 3);
}

.child-half {
  width: calc((100% - 45px) / 2);
}

.child-quarter {
  width: calc((100% - 75px) / 4);
  margin-bottom: 15px;
}
```

### التكليف 02

```html
<div class="normal">Normal</div>
<div class="one">One</div>
<div class="two">Two</div>
```

```css
div {
  margin: 20px auto;
  width: 300px;
  font-weight: bold;
  font-size: 1rem;
  padding: 20px;
  background-color: ???; /* Get The Background From Image */
  color: black;
}
```

- إستخدم البنية السابقة والتنسيقات الخاصة بها لعمل نفس الشكل
- خلفية جميع العناصر هي نفس خلفية العنصر الأول ولكن مع إختلاف الشفافية
- نسبة شفافية العنصرين الأخيرين هي 0.1 ولكن كيف تظهر الشكل كما في الصورة

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

div {
  margin: 20px auto;
  width: 300px;
  font-weight: bold;
  font-size: 1rem;
  padding: 20px;
  background-color: #b3b3b3;
  color: black;
}

.one {
  background-color: rgba(179, 179, 179, 0.1);
}

.two {
  opacity: 0.1;
}
```
