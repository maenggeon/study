# JavaScript란?
HTML 문서에 적용될 때, 웹사이트상에서 동적 상호작용성을 제공할 수 있는 완전한 동적 프로그래밍 언어.

## 자바스크립트 사용법
1. HTML 태그의 이벤트 리스너 속성에 작성
2. `<script> </script>` 태그에 작성
3. `<script src="파일경로" />`: script 태그안의 src속성에 자바스크립트(.js) 파일 경로 삽입
4. URL 부분에 작성

## 이벤트
: 사용자의 입력 행위를 브라우저가 웹페이지에 전달하는 수단 <br>
- 사용자가 HTML 태그가 출력된 영역에 키를 입력하거나 마우스를 클릭하면 이벤트가 발생하며, 이벤트는 해당 HTML 태그에게 전달

## 이벤트 리스너
: 이벤트를 처리하는 자바스크립트 코드
- ex) occlick, onchange, onmousemove 와 같이 이벤트 앞에 <b>on<b>을 붙인 이름

## 변수
: 여러 자료형을 담는 그릇. 변수의 어떠한 자료형도 저장할 수 있다.
- var <br>
  : 데이터 재할당, 재선언 가능. <br>
  특징
    ```
  - 함수 스코프(Function Scope)
  : 변수가 선언된 함수 안에서만 유효. 블록 { } 은 무시.
  
  - 호이스팅(Hoisting)
  : 변수 선언 전에 참조가 가능.(`undefined`)
  
  - 중복 선언 허용
  : 같은 스코프 내 같은 변수를 여러번 선언해도 덮어씌워지며 에러 발생 X.
  ```
- let <br>
  : 데이터 재할당 가능, 재선언 불가능. <br>
  특징
  ```
  - 블록 스코프(Block Scope)
  : 변수가 선언된 코드 블록 내에서만 유효.
  
  - 호이스팅(Hoisting) 불가
  
  - 중복 선언 불가
  ```
- const <br>
  : 상수 선언 시 사용.

## 자료형
#### Number
: 정수 및 부동소수점 숫자를 나타냄. <br>
- `특수 숫자값` 을 포함(`Infinity`, `-Infinity`, `NaN`)

#### String
- 큰따옴표(" "), 작은따옴표(' ')에 차이를 두지 않음.
- 역 따옴표(\` \`)
```
let name = world
alert( `Hello ${name}!` ); // Hello world!
```
#### Boolean
- true
- false

#### null
: 존재하지 않는 값, 비어있는 값을 나타날 때 사용.

#### undefined
: 값이 할당되지 않은 상태를 나타낼 때 사용.

#### 객체와 심볼
- 객체
  : 
- 심볼
  : 객체의 고유한 식별자를 만들 때 사용.

## 다이얼로그
- prompt("message", "default") <br>
  : 사용자한테 문자열을 입력받음. <br>
  : "default" 는 생략 가능. <br>

- alert("message") <br>
  : "message" 와 '확인' 버튼을 가진 다이얼로그 출력. <br>

- confirm("message") <br>
  : "message" 와 "확인/취소"사 버튼을 가진 다이얼로그 출력. <br>
  : "확인" 버튼은 true, "취소" 버튼은 false 를 리턴. <br>

## 함수(메서드)
`function` 키워드로 선언.
```JavaScript
function name(parameter, ...) {
    // 함수 본문
    return return_value;
}
```
: 함수 호출 시 매개변수에 인수를 전달하지 않으면 그 값은 `undefined` 로 초기화.
- 매개변수의 기본값
  ```JavaScript
  function name(parameter1, parameter2 = "기본값") {
      // 함수 본문
  }
  ```
  : `parameter2` 가 값을 전달받지 못하면 `기본값` 이 할당됨.
  
- 함수 선언문 방식
```JavaScript
function print_hello_world() {
    alert("Hello world!");
}
```

- 함수 표현식 방식
  : 함수는 값이기에 변수에 할당이 가능하다.
```JavaScript
let print_hello_world = function() {
    alert("Hello world!")
};
```

```JavaScript
function print_hello_world() {
    alert("Hello world!");
}
let func = print_hello_world; // 함수 복사

func(); // "Hello world!" 출력
print_hello_world(); // 본래 함수도 정상적으로 실
```
- 함수 표현식 vs 함수 선언문
  - 함수 생성 시간
    - 함수 표현식 : 실제 실행 흐름이 해당 함수에 도달했을 때 함수를 생성.
    - 함수 선언문 : 함수 선언문이 정의되기 전에도 호출 가능. <br>
    : 자바스크립트는 스크립트를 실행하기 전, 준비단계에서 전역에 선언된 함수 선언문을 찾고, 해당 함수를 생성함.
  - 스코프
    : 엄격 모드에서 함수 선언문은 블록 밖에서 접근하지 못함.

- 화살표 함수
  : `function` 키워드 대신 `=>` 를 사용하여 함수를 정의할 수 있음.
```JavaScript
// 일반 함수 표현식
const add = function(a, b) {
  return a + b;
};

// 화살표 함수
const add = (a, b) => {
  return a + b;
};
```
## 객체
: 데이터와 해당 데이터를 처리하는 메소드(함수)를 함께 포함하는 소프트웨어 구성요소. <br>
: 객체는 자신만의 고유한 속성을 가짐.
```JavaScript
let account = {
  //preperty
  owner     : "홍길동",
  code      : "111",
  balance   : 10000,

  //method
  deposit   : function() { ... },
  withdraw  : function() { ... },
  inquiry   : function() { ... }
};
```

### 자바스크립트 객체 유형
- 코어 객체 <br>
  : 기본 객체 <br>
  : Array, Date, String, Math 타입 등 <br>
  
- HTML DOM 객체 <br>
  : HTML 문서에 작성된 각 HTML 태그들을 객체화한 것들 <br>
  : HTML 문서의 내용과 모양을 제어하기 위한 목적 <br>

- 브라우저 객체 <br>
  : 브라우저를 제어하기 위해 제공되는 객체 <br>
  : 비표준 객체 <br>

### 코어 객체
- 코어 객체 생성 <br>
  : new 키워드 이용. <br>
  ```JavaScript
  let today = new Date();
  let msg = new String("Hello");
  ```
- 객체 접근 <br>
  : 객체와 멤버 사이에 점(.) 연산자 이용. <br>
  
- 배열 <br>
  : 여러 개의 원소들을 연속적으로 저장. <br>
  - 배열 크기 <br>
    : 배열 크기는 고정되지 않고 원소 추가 시 늘어남. <br>
    : 현재 배열보다 큰 인덱스에 원소를 추가하면 값이 비어있는 중간의 원소들도 생기는 문제 발생. <br>
      (비어있는 원소는 undefinde 값) <br>
    
  - [] 로 배열 만들기 <br>
  ```JavaScript
  let week = ["월", "화", "수", "목", "금", "토", "일"]
  ```
  - Array로 배열 만들기 <br>
  ```JavaScript
  let week = new Array(7);
  week[0] = "월";
  ...
  ```
  
- Date <br>
  : 날짜 및 시간 정보를 담는 객체 <br>

- String <br>
  : 문자열을 담기 위한 객체 <br>
  : String 객체는 생성되면 수정 불가능. <br>



- Math <br>
  :  <br>


## 이벤트
HTML 요소에서 발생한 사건.

