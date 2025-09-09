<img width="1203" height="605" alt="image" src="https://github.com/user-attachments/assets/ac2fcfb9-1495-4a58-891e-e9d085213c03" /> <br>
- `Content`  : 텍스트나 이미지가 들어가있는 HTML 요소의 실질적인 내용. <br>
- `Padding`  : `Content`와 `Border` 사이의 영역. 안쪽 여백. <br>
- `Border`  : `Content`를 감싸는 테두리. <br>
- `Margin`  : 테두리와 이웃하는 요소 사이의 간격. 바깥족 여백. <br>

## Content
- `width` : Content 영역의 가로 너비를 지정.
- `height` : Content 영역의 세로 너비를 지정.

## Padding
- `padding` : 안쪽 여백을 지정.
- `padding-{direction}` 속성을 사용해 원하는 방향마다 지정 가능.
  ### direction
  - top
  - left
  - right
  - bottom

## Border
- `border-style` : 테두리 스타일 지정
  - 4방향의 값을 한꺼번에 지정할 때는 방향 순서를 지켜야 함. top -> right -> bottom -> left
  - [테두리 스타일 종류](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)
- `border-width` : 테두리 두께 지정.
  - 값으로 `<크기>` 또는 키워드 `thin` `medium` `thick`
- `border-color` : 테두리 색상 지정.
- `border` : 단축 속성으로 `border-style` `border-width` `border-color`의 하위 속성을 포함.
  - `border-{direction}` 속성을 사용해 원하는 방향마다 지정 가능.
  - 예시
    ```css
    border: 1px solid red;
    border: 4px dashed green;
    ```
- `border-radius` : 테두리 꼭지점을 둥글게 만듦.

## Margin
- `margin` : 바깥 여백을 지정.
- `margin-{direction}` 속성을 사용해 원하는 방향마다 지정 가능.
  ### 마진중첩
  HTML 요소를 세로로 배치할 경우 `margin`과 `margin`이 만날 때, `margin`이 큰 쪽으로 요소가 겹쳐진다.

## Box Sizing
- HTML 요소의 너비와 높이를 계산하는 방법을 지정.
  - `content-box` : 기본 CSS 박스 크기 결정법. 콘텐츠 영역의 너비가 기준.
  - `border-box` : 테두리와 안쪽 여백도 고려. 콘테츠 영역의 크기가 줄어들 총 너비를 유지.
    ```css
    box-sizing: content-box;
    box-sizing: border-box;
    ```
