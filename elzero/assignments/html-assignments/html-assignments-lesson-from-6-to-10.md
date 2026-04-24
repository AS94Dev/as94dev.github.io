# تكليفات HTML الدروس من الدرس 06 إلى 10
## [ 7 ] تكليفات خاصة ب [ Heading And Attributes ]

### التكليف 01

1. ما هو ال السطر الذي يتم كتابته لتخبر المتصفح أن إصدار اللغة المستخدم في إنشاء الصفحة هو HTML5 ؟
```html
<!DOCTYPE html>
```
2. ما هو ال Rendering Mode الذي سوف يتبعه المتصفح إذا لم تكتب السطر الخاص بتحديد الإصدار ؟
`Quirks Mode`

3. هل من السليم إستخدام أكثر من h1 في الصفحة جاوب بنعم أو لا ؟ `(لا)`

4. لديك عنصر يحتوي على بيانات المنتج وعنوان المنتج مكتوب ب h3 هل من المنطقي وضع عنوان h2 داخل نفس المنتج أم لا؟ `(لا .. احط h4 لان الترتيب مهم عشان محركات البحث)`

5. إلى ماذا ترمز العناصر h1, h2, h3, h4, h5, h6
`Heading Elements`

### التكليف 02

```html
<p class="element">Welcome To The New World</p>
<p class='element'>Welcome To The New World</p>
<p class=element>Welcome To The New World</p>
```
- هل هناك إختلاف بين هذه العناصر عندما يتم إظهارهم في الصفحة أم لا ؟ 
`لا`

### التكليف 03

```html
<p class=element hidden>Welcome To The New World</p>
<p class="element" hidden>Welcome To The New World</p>
```
-  هل هناك إختلاف بين هذه العناصر عندما يتم إظهارهم في الصفحة أم لا ؟ 
`لا يوجد اختلاف في حالة ظهورهم .. لكنهم لن يظهروا لانه تم استخدام hidden وده وظيفته انه يخفي العنصر من الصفحة`

### التكليف 04

```html
<p>Hello World</p>

<p>
Hello World
</p>

<p>
Hello
World
</p>

<p>
Hello


World
</p>
```
-  هل هذه العناصر سوف تظهر كلها بنفس الشكل أم لا ؟ 
`هتظهر بشكل طبيعي كل فقرة في سطر وكل الكلمات جنب بعض مع مراعاة المسافات الداخلية .. اما المسافات والفراغات قبل وبعد عنصر p هيتم تجاهلها تماما.`

### التكليف 05

-  بجانب كل Attribute من الموجودين في المثال قم بكتابة هل هو من ال Global Attribute أم لا ؟ 
```html
title - Global
href - not Global
src - not Global
hidden - Global
charset - not Global
class - Global
id - Global
type - not Global
```
### التكليف 06

- قم بإنشاء صفحة كاملة تحتوي على كل ما درسناه سابقا
1. لدينا متجر ونريد كتابة عنوان المتجر في الصفحة إستخدم العنصر السليم لكتابة العنوان
2. تحت العنوان هناك فقرة نصية لوصف المتجر قم بكتابتها تحت العنوان مع إستخدام العنصر السليم
3. داخل المتجر هناك قسمين من المنتجات قم بكتابة عنوان القسم ولديك الحرية في كتابة أي عنوان تريد
4. تحت العنوان هناك 3 منتجات كل منتج له عنوان وفقرة نصية
5. بعد كل منتج قم بالفصل بينهم بخط فاصل hr

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Book Store</title>
    <meta name="description" content="a Small Book Store, we have all the books you are looking for." />
  </head>
  <body>
    <h1>Book Store</h1>
    <p>a Small Book Store, we have all the books you are looking for.</p>
    <h2>Programming</h2>
    <h3>Book 01</h3>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
    <hr>
    <h3>Book 02</h3>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
    <hr>
    <h3>Book 03</h3>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
    <hr>
    <h2>Self-Learning</h2>
    <h3>Book 01</h3>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
    <hr>
    <h3>Book 02</h3>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
    <hr>
    <h3>Book 03</h3>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</p>
    <hr>
  </body>
</html>
```

### التكليف 07
- قم بعمل الشكل الموجود في الصورة بال HTML فقط
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Page</title>
    <meta name="description" content="a Small Page i share my projects in." />
  </head>
  <body>
    <h1>My Page</h1>
    <p>This Is My Page</p>
    <p>This Is My First Work</p>
    <h2>Section One</h2>
    <p>This Is Section One</p>
  </body>
</html>
```