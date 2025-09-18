## Form Tag
웹에서 사용자의 정보를 입력받기 위해 사용.<br>
입력받는 데이터들의 묶음을 폼(Form), 데이터를 폼 데이터(Form Data) 또는 필드(Field) 라고 함.

### 속성
- `action` : 양식 데이터를 처리할 서버 프로그램의 URL
- `enctype` : 데이터 인코딩 타입
- `method` : 양식을 제출할 때 사용할 HTTP 메서드
  - `post` : 양식 데이터를 요청 본문으로 전송.
  - `get` : 양식 데이터를 URL의 쿼리스트링으로 붙여서 전송.
- `name` : 폼 이름
- `target` : 윈도우 이름

### Input Tag
`<form>`의 자식태그로서, `<input>` 요소로 데이터를 입력받을 수 있음.
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
         캡션 :
         <input type="text" id="data">
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
