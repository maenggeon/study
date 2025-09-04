# 선택자란?

## 기본 선택자
- 전체 선택자 <br>
  : 모든 요소에 스타일 적용.
  ```css
  * {
    color: blue;
  }
  ```
- Type 선택자 <br>
  : 해당 태그의 모든 요소에 스타일 적용.
  ```css
  p {
    color: blue;
  }
  ```
- Class 선택자 <br>
  : 해당 클래스의 모든 요소에 스타일 적용.
  ```html
  <span class="class-name"> ... </span>
  ```
  ```css
  .class-name {
    color: blue;
  }
  ```
- ID 선택자 <br>
  : 해당 ID의 요소에 스타일 적용. <br>
`ID 는 웹 문서에서 단 하나의 요소만 존재.`
  ```html
  <h1 id="id-name"> ... </h1>
  ```
  ```css
  #id-name {
    font-size: 40px;
  }
  ```
## 속성 선택자
주어진 속성을 가진 모든 요소를 검색.
- 문법 <br>
  - `[attr]` <br>
  : 속성 `attr` 이 존재하는 요소를 선택.

  - `[attr=value]` <br>
  : 속성 `attr` 값이 정확히 `value`인 요소를 선택.

  - `[attr~=value]` <br>
  : 속성 `attr` 값이 공백으로 구분된 단어 중 하나가 `value`인 요소를 선택.

  - `[attr|=value]` <br>
  : 속성 `attr` 값이 `value`이거나, `value-`로 시작하는 요소를 선택.

  - `[attr^=value]` <br>
  : 속성 `attr` 값이 `value`로 시작하는 요소를 선택.

  - `[attr$=value]` <br>
  : 속성 `attr` 값이 `value`로 끝나는 요소를 선택.

  - `[attr*=value]` <br>
  : 속성 `attr` 값이 `value`를 포함하는 요소를 선택.

## 그룹 선택자
선택자를 쉼표(,)로 구분해 여러 선택자를 나열함. <br>
같은 스타일을 여러 선택자에 한꺼번에 정의할 수 있다.
- 문법 <br>
  `선택자1, 선택자2 { 스타일 규칙 }`
- 예제
  ```css
  h1, h2 {
    text-align: center;
  }
  ```
  
## 결합자
### 자손 결합자
자손` `(공백) 결합자는 첫 번째의 요소의 자손인 태그를 선택.
- 문법 <br>
  `A B`
- 예제
  ```css
  /* <div> 태그 하위에 있는 모든 <span> 요소 */
  div span {
    color: blue;
  }
  ```
### 자식 결합자
자식`>` 결합자는 첫 번째의 요소의 바로 아래 자식인 태그를 선택.
- 문법 <br>
  `A > B`
- 예제
  ```css
  /* <ul> 태그의 바로 아래 자식인 모든 <li> 요소 */
  ul > li {
    color: blue;
  }
  ```
### 일반 형제 결합자
일반 형제`~` 결합자는 형제, 즉 첫 번째의 요소를 뒤따르면서 같은 부모를 공유하는 두 번째 요소를 선택.
- 문법 <br>
  `A ~ B`
- 예제
  ```css
  /* <p> 태그의 뒤에 나오는 모든 <span> 요소 */
  p ~ span {
    color: blue;
  }
  ```
### 인접 형제 결합자
일반 형제`+` 결합자는 형제, 즉 첫 번째의 요소의 바로 뒤에 위치하면서 같은 부모를 공유하는 두 번째 요소를 선택.
- 문법 <br>
  `A + B`
- 예제
  ```css
  /* 클래스 명이 "class_name"인 태그의 바로 뒤에 위치한 모든 <li> 요소 */
  .class_name + li {
    color: blue;
  }
  ```
