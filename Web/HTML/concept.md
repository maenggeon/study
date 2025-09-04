# 1.1 HTML 이란?
Hyper Text Markup Languagde 의 약자로서 태그(Tag)를 사용하여 웹페이지의 구조를 정의하는 웹 마크업 언어.

# 2.1 Tag
HTML 을 기술하기 위하여 사용하는 명령어 집합.

## 2.2 Tag 의 구성
`<태그이름 속성="값">콘텐츠</태그이름>`

## 2.3 HTML 문서 구조 관련 TAG
```html
<!DOCTYPE html> : 문서 타입 선언(HTML5)
<html> ... </html> : 전체 HTML 문서의 시작과 끝
<head> ... </head> : 문서의 메타데이(제목, 문자, 인코딩, CSS, JS 연결 등)
<title> ... </title> : 웹브라우저 탭에 표시될 제목.
<body> ... </body> : 실제 화면에 보여지는 콘텐츠가 들어가는 부분.
<!-- "..." --> : 주석
```
## 2.4 텍스트 관련 Tag
```html
<h1> ~ <h6>  Heading
: 웹 페이지의 제목 또는 부제목을 표현할 때 사용, 숫자가 을수록 큰 제목을 표시.
<p>  Paragraph
: 하나의 문단을 표시할 때 사용.
<hr>  Horizontal Rule
: 수평선(종료태그 X).
<br>  Break
: 줄바꿈(종료태그 X).
<b>  Bold
: 텍스트 진하게 표시.
<strong>
: 텍스트를 진하게 강조.
<i>  Italic
: 텍스트를 이텔릭체로 표시.
<em>  Emphasis
: 텍스트를 이텔릭체로 강조.
```
## 2.5 목록 관련 Tag
```html
<ol>  Ordered List
: 순서가 있는 목록을 표현할 때 사용.
<ul>  Unordered List
: 순서가 없는 목록을 표현할 때 사용.
<li>  Listed Item
: 목록하위 항목으로 사용되며, <ul>태그 또는 <ol>태그의 하위에 위치.
<dl>  Definition List
: 사전처럼 용어를 설명하는 목록을 생성.
<dt>  Definition Term
: 정의되는 용어 제목을 넣을 때 사용.
<dd>  Definition Description
: 용어를 설명하는 데 사용.
```
## 2.6 표 관련 Tag
```html
<table> : 표
<caption> : 표의 제목이나 설명을 붙일 때 사용하는 태그
<tr> : 행(row)
<th> : 제목 셀
<td> : 셀(cell)
```
## 2.7 영역 Tag
```html
<div> : 블록 레벨 요소.
<span> : 인라인 요소.
```
## 2.8 Semantic Tag
```html
<header> : 페이지에 대한 정보를 담는 태그. 페이지 상단에 위치.
<nav> : 네비세이션 링크로 구성된 섹션을 표현.
<aside> : main 과 분리된 내용을 담음.
<main> : 문서의 body 요소의 주 컨텐를 정의.
<section> : 문서나 응용프로그램의 일반적인 섹션을 표현.
<article> : 여러가지 아이템들을 묶어 재사용 가능하게 그룹화.
<footer> : 주로 저작권 정보나 서비스 제공자 정보들을 나타냄. 페이지 하단에 위치.
<details> : 추가적인 정보를 나타내거나 사용자가 요청하는 정보를 나타냄.
<summary> : 부모요소인 details 요소의 내용들에 대한 캡션, 혹은 제목을 나타냄.
<figure> : 일러스트, 다이어그램, 사진, 코드등에 주석을 다는 용도로 사용.
<figcaption> : 부모요소인 figure 요소의 내용들에 대한 캡션, 혹은 제목을 나타냄.
<mark> : 하나의 문서 내에서 다른 문맥과의 연관성을 나타내기 위해서 참조 목적으로 마킹되거나
         하이라이트된 텍스트를 표현.
<time> : 24시간에서의 시간 혹은 날짜를 나타냄.
```
## 2.9 멀티미디어 Tag
### 2.9.1 이미지 Tag
```html
<img> : HTML 문서에 이미지 삽입.
속성
- src (필수 O)
  : 이미지의 경로 저장
- alt
  : 이미지의 텍스트 설명. 웹 접근성 차원에서 매우 유용.
- height
  : 미지의 픽셀 단위 고유 크기.
- width
  : 이미지의 픽셀 단위 고유 너비.
```
### 2.9.2 오디오 Tag
```html
<audio> : HTML 문서에 소리 컨텐츠 삽입.
- src 속성을 사용
  <audio controls src="...">
- source 요소를 사용
  <audio controls>
    <source src="...">
  </audio>
```
### 2.9.3 비디오 Tag
```html
<video> : HTML 문서에 영상 컨텐츠 삽입.
- src 속성을 사용
  <video controls src="..." type="...">
- source 요소를 사용
  <video controls width="...">
    <source src="..." type="...">
  </video>
```
### 2.9.4 오디오&비디오 Tag 속성
```html
controls : 플레이어 화면에 컨트롤 바(재생막대)를 표시.
autoplay : 오디오나 비디오를 자동으로 실행.
loop : 오디오나 비디오를 반복 재생.
muted : 오디오나 비디오의 소리를 제거.
preload : 페이지를 불러올 때 오디오나 비디오 파일을 어떻게 로딩할 것인지 지정.
          (auto, metadata, none)
width / height : 비디오 플레이어의 너비와 높이를 지.
poster="파일 이름" : 비디오가 재생되기 전까지 화면에 표시될 포스터 이미지 지정.
```
### 2.9.5 하이퍼링크 Tag
```html
<a> : 다른 페이지나 같은 페이지의 특정 위치, 파일, 이메일 주소와 같은 다른 URL로
      연결할 수 있는 하이퍼링크를 생성.
속성
- href
  : 하이퍼링크가 가리키는 URL.
- target
  - _self : URL을 현재 브라우징 맥락에 표시. 기본값.
  - _blank : URL을 새로운 브라우징 맥락에 표시.
  - _parent : URL을 현재 브라우징 맥락의 부모에 표시.
  - _top : URL을 최상 브라우징 맥락에 표시.
```
## 2.10 Form Tag
웹에서 사용자의 정보를 입력받기 위해 사용.<br>
입력받는 데이터들의 묶음을 폼(Form), 데이터를 폼 데이터(Form Data) 또는 필드(Field) 라고 함.

### 속성
- `action` : 양식 데이터를 처리할 서버 프로그램의 URI
- `method` : 양식을 제출할 때 사용할 HTTP 메서드<br>
         - `post` : 양식 데이터를 요청 본문으로 전송.<br>
         - `get` : 양식 데이터를 URL의 쿼리스트링으로 붙여서 전송.<br>

### Input Tag
`<input>` 요소로 데이터를 입력받을 수 있음.
```html
<input type="text" id="name">
```
#### type
- `email` : email데이터를 받기 위해 사용(이메일 유효성 검증).
- `tel` : 전화번호를 받기 위해 사용.
- `password` : 비밀번호를 받기 위해 사용.(암호화 X)
- 더 많은 ['type'](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/input)

#### label
`<label>` 태그는 입력받는 필드를 설명할 때 사용.
- `<label>` 하위에 `<input>` 위치
 ```html
<label>
         이름 :
         <input type="text" id="name">
</label>
```
- `for`와 `id`속성을 사용하여 `<label>`과 연결.
```html
<label for="name">이름 : </label>
<input type="text" id="name">
```
#### fieldset
양식의 여러 컨트롤과 레이블`<label>`을 묶을 때 사용.

#### legend
요소는 부모 `<fieldset>` 콘텐츠의 설명을 나타냄.

### Form 데이터 Tag 속성
- `required` : 입력값이 필수임을 명시.
- `readonly` : 필드를 읽기 전용으로 만듦.
- `disabled` : 비활성화 시킬 수 있으며, 해당 필드는 서버로 전송 X
- `autofocus` : 초기에 해당 필드에 커서를 위치.
- `placehloder` : 입력 필드가 비어있을 때, 해당 입력값의 설명 또는 가이드 문구를 삽입.

#### checkbox
#### radio
#### Textarea
#### Select
#### datalist
#### Buttom
