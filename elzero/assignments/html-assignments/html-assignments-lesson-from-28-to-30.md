# تكليفات HTML الدروس من الدرس 28 إلى 30

## [ 3 ] تكليفات خاصة ب [ Form Part Two ]

### التكليف 01 & التكليف 02 & التكليف 03

- قم بإنشاء نموذج يحتوي على ثلاث حقول إدخال
- كل حقل يجب أن يحتوي على Label قبله
- الحقول هي Token, Email, Username
- تأكد أن حقل ال Token حقل مخفي ويحتوي على القيمة التالية b92f1fc2fce391ad7af633723afd3055
- تأكد أن حقل ال Email لا يمكن التعديل عليه ويكون به القيمة التالية o@o.com
- عند فتح الصفحة تأكد أن مؤشر الكتابة مركز عند الحقل Username
- تأكد من أن حقل Username يقبل إسم مستخدم من 5 حروف إلى 20 حرف فقط ويكون إجباري
- قم بعمل زر يقوم بإفراغ محتوى البيانات التي كتبها المستخدم ويكون إسمه Empty
- قم بعمل زر لإرسال البيانات بإسم Send
- يتم إرسال البيانات لنفس الصفحة
- قم بإضافة ما يلي للنموذج السابق
- قائمة من الإختيارات Check تخص مهارات برمجية يمكن أن يختار الشخص منها أكثر من مهارة
- على سبيل المثال Problem Solving, Logical Thinking, Advanced Search, Analysis, Planning
- يجب أن يكون ال Label مرتبط بالإختيار بمعنى عند الضغط على ال Label يتم تفعيل الإختيار
- قم بإنشاء قائمة أخرى من الإختيارات تخص وظيفة الشخص ويجب إختيار خيار واحد فقط منها
- على سبيل المثال Front-End Developer, Back-End Developer, Business Analyst, Project Manager, Scrum Master
- يجب أن يكون ال Label مرتبط بالإختيار بمعنى عند الضغط على ال Label يتم تفعيل الإختيار
- قائمة الخيارات الأولى يكون إسمها skills
- قائمة الإختيارات الثانية يكون إسمها job
- في كل خيار من الخيارات يجب أن يكون هناك خيار واحد على الأقل Checked
- قم بإضافة ما يلي للنموذج السابق
- قائمة من الخيارات تخص المجال البرمجي فيها مجموعة لغات برمجة بإصداراتهم لتختار من بينهم
- شاهد الصورة لتقوم بعمل المهمة مثل الصورة
- بعدها قم بإنشاء حقل يقبل كتابة نص طويل جدا ويكون إسمه brief
- الحقل يحتوي على نص مسبق لتوضيح ما سوف يتم كتابته وقيمته هي Write Here Why You Want To Learn Programming

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Dummy Form</title>
  </head>
  <body>
    <form action="" method="get">
      <!-- التكليف 01 -->
      <div>
        <input type="hidden" name="token" value="b92f1fc2fce391ad7af633723afd3055" />
      </div>
      <div>
        <label>Email</label>
        <input type="email" name="email" value="o@o.com" readonly />
      </div>
      <div>
        <label>Username</label>
        <input type="text" name="username" minlength="5" maxlength="20" required autofocus />
      </div>
      <hr />
      <!-- التكليف 02 -->
      <h2>Skills</h2>
      <div>
        <input type="checkbox" id="skill1" name="skills" checked />
        <label for="skill1">Problem Solving</label>
      </div>
      <div>
        <input type="checkbox" id="skill2" name="skills" />
        <label for="skill2">Logical Thinking</label>
      </div>
      <div>
        <input type="checkbox" id="skill3" name="skills" />
        <label for="skill3">Advanced Search</label>
      </div>
      <div>
        <input type="checkbox" id="skill4" name="skills" />
        <label for="skill4">Analysis</label>
      </div>
      <div>
        <input type="checkbox" id="skill5" name="skills" />
        <label for="skill5">Planning</label>
      </div>
      <hr />
      <h2>Job Title</h2>
      <div>
        <input type="radio" id="job1" name="job" checked />
        <label for="job1">Front-End Developer</label>
      </div>
      <div>
        <input type="radio" id="job2" name="job" />
        <label for="job2">Back-End Developer</label>
      </div>
      <div>
        <input type="radio" id="job3" name="job" />
        <label for="job3">Business Analyst</label>
      </div>
      <div>
        <input type="radio" id="job4" name="job" />
        <label for="job4">Project Manager</label>
      </div>
      <div>
        <input type="radio" id="job5" name="job" />
        <label for="job5">Scrum Master</label>
      </div>
      <hr />
      <!-- التكليف 03 -->
      <label for="book">Choose Book:</label>
      <select name="book" id="book">
        <optgroup label="PHP">
          <option>v5.0</option>
          <option>v7.0</option>
          <option>v8.0</option>
        </optgroup>
        <optgroup label="Python">
          <option>v2.0</option>
          <option>v3.0</option>
          <option>v3.9</option>
        </optgroup>
      </select>
      <hr />
      <textarea name="brief" id="brief" rows="10" cols="50">Write Here Why You Want To Learn Programming</textarea>
      <br />
      <input type="reset" value="Empty" />
      <input type="submit" value="Send" />
    </form>
  </body>
</html>
```
