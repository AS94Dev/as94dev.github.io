# تكليفات HTML الدروس من الدرس 11 إلى 14

## [ 4 ] تكليفات خاصة ب [ Link, Image, List ]

### التكليف 01

- يمكنك كتابة أي إسم بدلا من الإسم الموجود في الصورة وإضافة أي رابط بدل الموجود في الصورة
- يجب التأكد أن إسمك بخط عريض فقط وليس شيء مهم وكلمة Available بخط عريض ولكنها رسالة مهمة
- يجب فتح الرابط في صفحة جديدة.
- يجب إستعمال عناصر ال HTML فقط لعمل المطلوب

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Info</title>
  </head>
  <body>
    <h2>My Info</h2>
    <p>My name is: <b>Abdallah Sayed</b></p>
    <p>I'm <strong>Available</strong> for hire</p>
    <p>My hour old price is <del>$10</del>, The new price is <mark>$30</mark></p>
    <p>Visit my website from this link <a href="https://as1994.netlify.app/" target="_blank">&lt; as1994 &#47;&gt;</a></p>
    <hr />
    <h2>Here Is Some Of My Clients</h2>
    <img src="https://placehold.co/50x50/ff0000/FFF" alt="Client placeholder img" />
    <img src="https://placehold.co/50x50/0000ff/FFF" alt="Client placeholder img" />
    <img src="https://placehold.co/50x50/00ff00/FFF" alt="Client placeholder img" />
    <hr />
    <h2>My Skills</h2>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>
        JavaScript
        <ul>
          <li>Vuejs</li>
          <li>Reactjs</li>
          <li>
            Angular
            <ol>
              <li value="4">v4.0</li>
              <li>v5.0</li>
              <li>v6.0</li>
              <li>v7.0</li>
              <li>v8.0</li>
            </ol>
          </li>
          <li>Svelte</li>
        </ul>
      </li>
      <li>Python</li>
    </ul>
  </body>
</html>
```

### التكليف 02

- قم بعمل الشكل الموجود في الصورة بال HTML فقط
- يجب عمل الترقيم بال HTML ولا تكتبه بنفسك

```html
<ul>
  <li>
    One
    <ol start="3" type="A">
      <li>C</li>
      <li>D</li>
      <li>E</li>
    </ol>
  </li>
  <li>
    Tow
    <ol start="3" type="I">
      <li>3</li>
      <li>4</li>
      <li>5</li>
    </ol>
  </li>
  <li>
    Three
    <ol start="4" type="a" reversed>
      <li>d</li>
      <li>c</li>
      <li>b</li>
    </ol>
  </li>
</ul>
```

### التكليف 03

- قم بكتابة جميع إستخدامات ال Anchor التي تعرفها
- شاهد أول مثال لترى الفكرة

```html
<!-- Go To External Link -->
<a href="https://google.com">Google</a>

<!-- go to section or paragraph on the same page with id one -->
<a href="#one">Google</a>

<!-- open the mail app and add the mail in the to section -->
<a href="mailto:contact@as94.me">Contact Me</a>

<!-- Go to page called test in the same project's folder -->
<a href="test.html" title="Go To Test Page">Test</a>
```

### التكليف 04

- قم بعمل الشكل الموجود في الصورة بال HTML فقط
- يجب عمل الشكل بالعنصر المناسب لهذا الشكل

```html
<dl>
  <dt>Learn Programming</dt>
  <dd>Learn Computer Science</dd>
  <dd>Learn Database</dd>
</dl>
<dl>
  <dt>Design</dt>
  <dd>Learn Graphics</dd>
  <dd>Learn Sketching</dd>
</dl>
```
