# JavaScript란?
HTML 문서에 적용될 때, 웹사이트상에서 동적 상호작용성을 제공할 수 있는 완전한 동적 프로그래밍 언어.

## 자바스크립트 사용법
- `<script src="파일경로" />`: script 태그안의 src속성에 자바스크립트 파일 경로 삽입
  
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
- let
  : 데이터 재할당 가능, 재선언 불가능. <br>
  특징
  ```
  - 블록 스코프(Block Scope)
  : 변수가 선언된 코드 블록 내에서만 유효.
  
  - 호이스팅(Hoisting) 불가
  
  - 중복 선언 불가
  ```
- const
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

## 기본 팝업창
- alert
  : 사용자가 '확인' 버튼을 누를 때까지 메시지를 보여주는 창을 띄움.
- prompt
  : 사용자한테 문자열을 입력받을 때 사용.
- confirm
  : 사용자한테 boolean 값을 입력받을 때 사용.

## 함수(메서드)
자바스크립트에선 함수를 특별한 종류의 값으로 취급. <br>
`function` 키워드로 선언.
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
    alert("Hello world!");
};
```

```JavaScript
function print_hello_world() {
    alert("Hello world!");
}
let func = print_hello_world; // 함수 복

func(); // "Hello world!" 출력
print_hello_world(); // 
```

## 객체

## 이벤트
HTML 요소에서 발생한 사건.

