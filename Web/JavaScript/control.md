## HTML 요소 선택하기
### get 메서드
- `document.getElementById`: 모든 HTML 요소에는 고유한 ID를 할당 가능. ID를 이용해 요소를 찾을 수 있음.
- `document.getElementsByClassName`: HTML 클래스 명으로 요소를 찾을 수 있음.
- `document.getElementsByTagName`: HTML 태그명으로 요소를 찾을 수 있음.

### DOM 요소 쿼리
CSS 선택자를 사용해 요소를 찾는 메서드.
- `document.querySelector`: 지정된 선택자에 일치하는 문서 내 첫번째 요소를 반환. 일치하는 요소가 없을시 null을 반환
- `document.querySelectorAll`: 지정된 선택자에 일치하는 요소 목록을 반환.

## HTML 요소 조작하기
### 콘텐츠 수정하기
