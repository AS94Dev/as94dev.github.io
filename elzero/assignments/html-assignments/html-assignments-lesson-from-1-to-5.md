# تكليفات HTML الدروس من الدرس 01 إلى 05

## [ 4 ] تكليفات خاصة ب [ Elements And Comments ]

### التكليف 01

1.  ما الذي ترمز إليه كلمة HTML

- HTML = HyperText Markup Language.

### التكليف 02

1. قم بإنشاء صفحة كاملة فيها جميع العناصر التالية html, head, body
2. قم بإنشاء عنوان للصفحة بإسم My First Page
3. قم بوضع وصف الصفحة الذي يظهر في المتصفحات This Is Description For My First Page
4. قم بوضع العنصر الذي يتم كتابة CSS Code داخله ويمكن تركه فارغا
5. قم بوضع العنصر الذي يتم كتابة JavaScript Code داخله ويمكن تركه فارغا
6. قم بوضع العنصر المسؤول عن إستدعاء ملف CSS خارجي
   قم بكتابة نص This Is My First Page بحيث يظهر داخل الصفحة

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My First Page</title>
    <meta name="description" content="This Is Description For My First Page" />
    <style></style>
    <script></script>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1>This Is My First Page</h1>
  </body>
</html>
```

### التكليف 03

- قم بالإجابة على الأسئلة التالية بنعم أو لا

1. هل ما يتم كتابته داخل ال Head يظهر داخل الصفحة أم لا؟ (لا)
2. هل عنصر Title له قفلة أم لا ؟ (نعم)
3. هل عنصر Meta له قفلة أم لا ؟ (لا)
4. هل ما يتم وضعه داخل ال Description في عنصر ال Meta يظهر في الصفحة أم لا ؟ (لا)

### التكليف 04

- قم بكتابة 4 عناصر Meta داخل ال Head مع شرح كل فائدة كل واحد فيهم عن طريق Multiple Line Comment

```html
<meta charset="UTF-8" />
<!--
تحديد الترميز الخاص بالصفحة
نستخدم هنا الترميز العالمي Unicode Transformation Format
الذي يدعم جميع اللغات والأحرف الخاصة بها
-->

<meta name="description" content="Your Website Description"/>
<!--
وضع وصف الصفحة فعندما تبحث عن موقع معين في Google
تجد إسم الموقع وتحته نص يوصف الموقع
-->

<meta name="copyright" content="Your Company Or Brand Name" />
<!--
تخبر الشخص الذي يتصفح موقعك أنه لديك مواد عليها حقوق فكرية Copyright
وهي مملوكة لشركتك أو موقعك المكتوب داخل ال Content
-->

<meta name="author" content="Elzero" />
<!--
هو المؤلف أو الكاتب الذي كتب محتوى الصفحة 
-->
```
