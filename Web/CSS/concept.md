# CSS란?
Cascading Style Sheets 의 약자로, 마크업 언어로 작성된 문서의 표현과 스타일을 지정하는 스타일 시트 언어.

## 구조
선택자{
  속성명: 속성값;
}

## 적용 방법
- Inline Style Sheet
```html
<h1 style="color: blue">파랑</h1>
```
- Internal Style Sheet
```html
...
<head>
  <style>
    h1 {
      color: blue;
    }
    .content {
      background-color: yellow;
      padding: 10px;
    }
  </style>
</head>
<body>
  <h1>파랑</h1>
  <p class="content">본문</p>
</body>
...
```
- External Style Sheet
```html
<head>
  ...
  <link rel="stylesheet" href="style.css">
</head>
```
```css
/* style.css */
h1 {
  color: blue;
}
.content {
  background-color: yellow;
  padding: 10px;
}
```

## 출처
- Author Style <br>
  웹 사이트를 제작하는 `제작자가 작성한 스타일 시트`.
- User Style <br>
  사이트를 방문하는 일반 `사용자들이 구성한 스타일 시트`.
- Browser Style <br>
  `브라우저`들마다 기본적으로 저장하고 있는 스타일.

### 적용 우선순위
`사용자 !important` > `제작자 !important` > `제작자` > `사용자` > `브라우저`
