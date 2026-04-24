# تكليفات HTML الدروس من الدرس 31 إلى 34

## [ 4 ] تكليفات خاصة ب [ Form Part Three ]

### التكليف 01

- قم بإنشاء نموذج يحتوي على ثلاث حقول إدخال
- كل حقل يجب أن يحتوي على Label قبله
- الحقول هي Search, File, URL
- تأكد أن حقل ال Search يحتوي على رسالة للشخص بالمحتوى التالي Enter A Search Word
- عند فتح الصفحة تأكد أن مؤشر الكتابة مركز عند الحقل Search
- تأكد من أن حقل URL لحتوي على ال Attribute الخاص بجعل الحقل إجباري
- قم بعمل زر يقوم بإفراغ محتوى البيانات التي كتبها المستخدم ويكون إسمه Empty
- تأكد أن البيانات داخل النموذج يتم إرسالها في Tab جديدة وليس في نفس الصفحة
- تأكد أن الشخص لو لم يكتب أي قيمة في حقل ال URL سوف يتم تجاهل ال Required Attribute ويتم إرسال البيانات بدون مشكلة
- شاهد الشكل النهائي المطلوب

### التكليف 02

- قم بإضافة حقلين للنموذج السابق
- الحقول هي Date, Month
- يجب أن يكون القيمة الإفتراضية لحقل ال Date هي 25/10/1982
- يجب أن تكون القيمة الإفتراضية لحقل الشهور هي October 1982
- شاهد الشكل النهائي المطلوب

```html
<form action="" target="_blank" novalidate method="get">
  <div>
    <label for="search">Search</label>
    <br />
    <input type="search" id="search" placeholder="Enter A Search Word" autofocus />
  </div>
  <br />
  <div>
    <label for="file">File</label>
    <br />
    <input type="file" id="file" />
  </div>
  <br />
  <div>
    <label for="url">URL</label>
    <br />
    <input type="url" id="url" required />
  </div>
  <br />
  <div>
    <label for="date">Date</label>
    <input type="date" id="date" value="1982-10-25" />
  </div>
  <br />
  <div>
    <label for="month">Month</label>
    <input type="month" id="month" value="1982-10" />
  </div>
  <br />
  <input type="reset" value="Empty" />
  <input type="submit" value="Send" />
</form>
```

### التكليف 03

- قم بكتابة النص التالي وتأكد أنه سوف يظهر في المتصفح كما في الصورة التالية. يجب عليك وضع الأربعة أسطر في عنصر واحد فقط

```html
<pre>
  Hello Line One
  Hello Line Two
  Hello Line Three
    Hello Line Four
</pre>
```

### التكليف 04

- قم بإستدعاء موقع Elzero داخل صفحتك مع جعل عرض الموقع يملأ الشاشة والطول يكون 400 Pixel. شاهد الصورة لترى المطلوب

```html
<iframe src="https://elzero.org" frameborder="0" width="100%" height="400"></iframe>
```
