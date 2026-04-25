# تكليفات HTML الدروس من الدرس 24 إلى 27

## [ 2 ] تكليفات خاصة ب [ Form Part One ]

### التكليف 01

- قم بإنشاء نموذج يحتوي على خمس حقول إدخال
- كل حقل يجب أن يحتوي على Label قبله
- الحقول هي Username, Password, Mobile, Email, Subject
- تأكد من إختيار نوع الحقل المناسب لكل مما سبق
- حقل ال Mobile يمكن أن يحتوي على رقم بهذا الشكل +20100 (234) 123
- حقل ال Username + Email إجباري كتابته
- جميع الحقول يجب أن تحتوي على نص يوجه الشخص لنصائح أثناء ملأ الحقل. يمكنك كتابة ما تريد في النصائح
- يجب أن يكون ال Label على سطر وحقل الإدخال على سطر آخر تحته
- كل Label + Input يجب وضع hr بعدهم للفصل بينهم وبين ال Label + Input الموجودين بعدهم
- البيانات الموجودة في النموذج سوف يتم إرسالها لصفحة اسمها test.py
- يجب التأكد ان البيانات التي يتم إرسالها لن تظهر في الرابط العلوي
- قم بإلتقاط صورة من ال Query String التي تحتوي على البيانات
- يجب عليك وضع حقل مخفي تكون قيمته أي رقم تريده
- يجب وضع زر يقوم بحذف جميع ما تم كتابته في حقول الإدخال ويكون إسمه Empty Form
- يجب وضع زر لإرسال البيانات يكون إسمه Send Data

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Form Elements</title>
  </head>
  <body>
    <form action="test.py" method="post">
      <input type="hidden" value="I &hearts; Elzero" name="token" />
      <div>
        <label>Username</label>
        <br />
        <input type="text" name="Username" required placeholder="ex: Abdallah Sayed" />
      </div>
      <hr />
      <div>
        <label>Password</label>
        <br />
        <input type="password" name="Password" placeholder="Write a complex password" />
      </div>
      <hr />
      <div>
        <label>Mobile</label>
        <br />
        <input type="tel" name="Mobile" value="+20100 (234) 123" placeholder="ex: +20100 (234) 123" />
      </div>
      <hr />
      <div>
        <label>Email</label>
        <br />
        <input type="email" name="Email" required placeholder="ex: example@email.com" />
      </div>
      <hr />
      <div>
        <label>Subject</label>
        <br />
        <input type="text" name="Subject" placeholder="ex: Problem with X" />
      </div>
      <hr />
      <input type="reset" value="Empty Form" />
      <input type="submit" value="Send Data" />
    </form>
  </body>
</html>
```

### التكليف 02

- قم بعمل الشكل الموجود في الصورة بال HTML فقط
- القيمة الإفتراضية هي 400
- لا تحتاج لعمل الأرقام هي فقط لتوضيح المطلوب

```html
<form>
  <input type="range" value="400" min="100" max="500" step="50" />
</form>
```
