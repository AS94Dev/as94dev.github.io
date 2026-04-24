# تكليفات HTML الدروس من الدرس 15 إلى 18

## [ 3 ] تكليفات خاصة ب [ Table, Div ]

### التكليف 01

- تأكد أن الجدول يملأ الشاشة كاملة
- يمكنك كتابة أي أسماء وبيانات تريدها
- حجم الصورة يجب أن يكون 40×40
- يمكنك وضع اي رابط تريده لا توجد مشكلة ولكن أهم شيء أن يفتح الرابط في صفحة جديدة
- يجب إستعمال عناصر ال HTML فقط لعمل المطلوب
- يجب أن يكون الإسم الأول على سطر والثاني على سطر تحته
- الشخص الأول لديه أكثر من Email يجب وضع خط فاصل بينهم
- قم بإضافة Caption للجدول يحتوي على جملة Members Data

```html
<table width="100%" border="1">
  <caption>
    Members Data
  </caption>
  <tr>
    <th>Group</th>
    <th>Avatar</th>
    <th>Name</th>
    <th>Email</th>
    <th>Character</th>
    <th>Profile</th>
  </tr>
  <tr>
    <td rowspan="2">Ninja</td>
    <td><img src="https://placehold.co/40x40/ff0000/FFFFFF/png" alt="" /></td>
    <td>Osama <br />Mohamed</td>
    <td>
      o1@nn.sa
      <br />
      <hr />
      o2@nn.sa
    </td>
    <td>&copy;</td>
    <td><a href="http://as1994.netlify.app/" target="_blank">Profile</a></td>
  </tr>
  <tr>
    <td><img src="https://placehold.co/40x40/0000ff/FFFFFF/png" alt="" /></td>
    <td>Shady <br />Nabil</td>
    <td>s@nn.sa</td>
    <td>&trade;</td>
    <td><a href="http://as1994.netlify.app/" target="_blank">Profile</a></td>
  </tr>
  <tr>
    <td>Monsters</td>
    <td><img src="https://placehold.co/40x40/000000/FFFFFF/png" alt="" /></td>
    <td>Mohamed <br />Ibrahim</td>
    <td>m@nn.sa</td>
    <td>&reg;</td>
    <td><a href="http://as1994.netlify.app/" target="_blank">Profile</a></td>
  </tr>
  <tr>
    <td colspan="5">Total Members</td>
    <td>3</td>
  </tr>
</table>
```

### التكليف 02

- قم بعمل الشكل الموجود في الصورة بال HTML فقط

```html
<table border="1" cellspacing="1" cellpadding="20">
  <caption>
    Members Points
  </caption>
  <tr>
    <th>Data</th>
    <th>Name</th>
    <th>Points</th>
  </tr>
  <tr>
    <td rowspan="4">Month</td>
    <td>Osama Mohamed</td>
    <td>100</td>
  </tr>
  <tr>
    <td>Sayed Mohamed</td>
    <td>100</td>
  </tr>
  <tr>
    <td>Ahmed Mohamed</td>
    <td>100</td>
  </tr>
  <tr>
    <td>Eman Mohamed</td>
    <td>100</td>
  </tr>
</table>
```

### التكليف 03 (تحدي)

- قم بعمل الشكل الموجود في الصورة بال HTML فقط

```html
<table border="1" cellspacing="2" cellpadding="10">
  <caption>
    Complex Table
  </caption>
  <tr>
    <th>Year</th>
    <th>Group</th>
    <th>Language</th>
    <th>Done</th>
    <th>Passed</th>
  </tr>
  <tr>
    <td rowspan="5">2022</td>
    <td rowspan="2">Elzero</td>
    <td>HTML</td>
    <td colspan="2">Yes</td>
  </tr>
  <tr>
    <td>CSS</td>
    <td colspan="2">Yes</td>
  </tr>
  <tr>
    <td rowspan="3">Heroes</td>
    <td>JS</td>
    <td>Yes</td>
    <td>No</td>
  </tr>
  <tr>
    <td>PHP</td>
    <td colspan="2">yes</td>
  </tr>
  <tr>
    <td>Python</td>
    <td>No</td>
    <td>No</td>
  </tr>
</table>
```
