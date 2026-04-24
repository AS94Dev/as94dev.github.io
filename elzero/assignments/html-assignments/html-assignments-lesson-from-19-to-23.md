# تكليفات HTML الدروس من الدرس 19 إلى 23

## [ 4 ] تكليفات خاصة ب [ Audio, Video ]

### التكليف 01

- ما هي العناصر الموجودة في اللغة من العناصر التالية

```html
<!-- 
  Header -> HTML
  Nav -> HTML
  Main -> HTML
  Aside -> HTML
  Picture -> HTML
  Figure -> HTML
  Footer ->  HTML
  FigCaption -> HTML
  Section -> HTML
  Command -> not HTML
  Ruby -> HTML (not use much)
  Data -> HTML
  Article -> HTML
  Install -> not HTML
  Text -> not HTML
-->
```

### التكليف 02

- قم بإنشاء صفحة كاملة جديدة
- تأكد أنك تستخدم ال Semantic Elements في جميع الطلبات التالية
  قم بإنشاء Header يحتوي على عنوان الصفحة والروابط الخاصة بالصفحة
- يمكنك وضع خمس روابط بأي أسماء
- تحتها قم بعمل Navigation Bar يحتوي على مجموعة روابط على الأقل 6 روابط بأي أسماء
- قم بعمل عنصر يحتوي على محتوى الصفحة وبجانبه عنصر يحتوي على محتوى ال Sidebar
- داخل محتوى الصفحة قم بعمل ثلاثة مقالات كل مقال بينه وبين الآخر خط عرضي
- في كل مقال قم بوضع عنوان للمقال وتحته فقرة نصية فيها جزء من محتوى المقال
- تحتها صورة للمقال ثم تحتها رابط فيه كلمة إقرأ المزيد
  في أسفل الصفحة قم بإنشاء عنصر لل Footer وداخله جملة Copyright 2021 ©
- وتأكد أنك تستخدم ال Entity السليمة لل Character
- داخل عنصر ال Sidebar قم بوضع عنوان بإسم Categories
- تحت العنوان إستخدم Unordered List لوضع خمس أقسام بأي اسماء تريد

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Semantic Elements</title>
  </head>
  <body>
    <header>
      <h1>My Portfolio</h1>
      <nav>
        <a href="#">Home</a>
        <a href="#">About Me</a>
        <a href="#">Projects</a>
        <a href="#">Articles</a>
        <a href="#">Contact/Hire Me</a>
      </nav>
    </header>
    <main>
      <aside>
        <h2>Categories</h2>
        <ul>
          <li>About Me</li>
          <li>Projects</li>
          <li>Articles</li>
        </ul>
      </aside>
      <section>
        <h2>Articles</h2>
        <hr />
        <article>
          <h3>Lorem ipsum</h3>
          <p>dolor sit, amet consectetur adipisicing elit...</p>
          <a href="#">Read More!</a>
          <img src="https://placehold.co/600x400/000000/FFFFFF/png" alt="Article Image" />
          <hr />
        </article>
        <article>
          <h3>Lorem ipsum</h3>
          <p>dolor sit, amet consectetur adipisicing elit...</p>
          <a href="#">Read More!</a>
          <img src="https://placehold.co/600x400/000000/FFFFFF/png" alt="Article Image" />
          <hr />
        </article>
        <article>
          <h3>Lorem ipsum</h3>
          <p>dolor sit, amet consectetur adipisicing elit...</p>
          <a href="#">Read More!</a>
          <img src="https://placehold.co/600x400/000000/FFFFFF/png" alt="Article Image" />
          <hr />
        </article>
      </section>
    </main>
    <footer>
      <p>Copyright 2021 &copy;</p>
    </footer>
  </body>
</html>
```

### التكليف 03 / التكليف 04

- قم بإضافة عنصر يحتوي على ملف صوتي بأكثر من إمتداد 3 Extensions
- قم بإضافة عنصر يحتوي على ملف فيديو بأكثر من إمتداد 3 Extensions
- ضع رسالة تظهر في حالة كان المتصفح لا يدعم الملف الصوتي
- ضع رسالة تظهر في حالة كان المتصفح لا يدعم الملف المرئي
- تأكد ان الملف يعمل تلقائيا عند فتح الصفحة
- تأكد أن الملف إذا إنتهي سوف يعمل تلقائيا مرة أخرى
- تأكد أن الفيديو لا يوجد به صوت عندما يعمل
- ضع في ال Caption لغتين يمكن الشخص أن يختارهم
- ضع Poster للفيديو باي صورة تريدها يظهر عند التحميل

```html
<!-- audio -->
<audio controls autoplay loop>
  <source src="audio-file.mp3" type="audio/mpeg" />
  <source src="audio-file.ogg" type="audio/ogg" />
  <source src="audio-file.wav" type="audio/wav" />
  عذراً، متصفحك لا يدعم تشغيل ملفات الصوت. يمكنك تحميل الملف بدلاً من ذلك.
</audio>

<!-- video -->
<video width="640" height="360" autoplay loop muted poster="https://via.placeholder.com/640x360.png?text=Loading+Video..." controls>
  <source src="movie.mp4" type="video/mp4" />
  <source src="movie.webm" type="video/webm" />
  <source src="movie.ogv" type="video/ogg" />
  <track src="captions_ar.vtt" kind="captions" srclang="ar" label="العربية" default />
  <track src="captions_en.vtt" kind="captions" srclang="en" label="English" />
  عذراً، متصفحك لا يدعم تشغيل ملفات الفيديو. يمكنك تحميل الفيديو لمشاهدته.
</video>
```
