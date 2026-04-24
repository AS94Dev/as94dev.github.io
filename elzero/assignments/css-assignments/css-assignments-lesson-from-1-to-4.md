# تكليفات CSS الدروس من 01 إلى 04

## [ 6 ] تكليفات خاصة ب [ Elements And Naming ]

### التكليف 01

- اكتب في تعليق كل Selector ما الذي يعبر عنه

```css
/* Any Element With Class Title */
.title {
}

/* Element with id nav */
#nav {
}

/* Any div Element */
div {
}

/* any h2 Element */
h2 {
}
```

### التكليف 02

- اكتب في تعليق نوع كل Style من التالي

```html
<!-- external css -->
<link rel="stylesheet" href="css/file.css" />

<!-- enteral css -->
<style>
  p {
    color: red;
  }
</style>

<!-- inline css -->
<p style="color: blue;">This Is Our Paragraph</p>
```

### التكليف 03

- قم بإستدعاء ملف Style خارجي موجود في مجلد بجانب ال index.html بإسم assets وداخله مجلد باسم css وإسم الملف هو master.css

```html
<!-- Write Path -->
<link rel="stylesheet" href="assets/css/master.css" />
```

### التكليف 04

- قم بإستدعاء ملف Style خارجي موجود في مجلد خارج المجلد الموجود فيه ملف ال index.html بإسم source وداخله مجلد بإسم css وإسم الملف هو main.css

```html
<!-- Write Path -->
<link rel="stylesheet" href="../source/css/main.css " />
```

### التكليف 05

- في أسماء ال Identifiers التالية حدد ما هو صالح وما هو غير صالح عن طريق كتابة Valid أو Not Valid في التعليق قبل الإسم

```css
/* Valid */
._user-name {
}

/* Valid */
.-user-name {
}

/* Not Valid */
.1user-name {
}

/* Not Valid */
.@user-name {
}

/* Not Valid */
.user@name {
}

/* Valid */
._user10name {
}

/* Valid */
.u {
}
```

### التكليف 06

- في أسماء ال Identifiers التالية حدد ما الذي يتبع ال Best Practice عن طريق كتابة Good أو Bad في التعليق قبل الإسم

```css
/* Bad */
.USERNAME {
}

/* Good */
.UserName {
}

/* Good */
.user-name {
}

/* Good */
.userName {
}

/* Bad */
.usernameprofile {
}
```
