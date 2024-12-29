- `flexbox`는 정렬의 끝판왕
- 원리 이해보다는 잘 사용하는 방법에 대해서만 알아도 됨.
- 알아둬야할 4가지 원칙
  1. "나, 플렉스 박스 쓸거야"
  2. "가로 정렬? 세로 정렬?"
  3. "무조건 한 줄 안에 다 정렬?"
  4. "신나는 플렉스박스 파티 타임!"

## "나 플렉스박스 쓸거야"

```css
.flexbox {
  display: flex;
  /* display: inline-flex; */ /* <- inline block과 유사 */
}
```

- 블록과 유사하되, 블록에서는 할 수 없는 정렬 기능을 수행
- 정렬을 하고자 하는 요소를 감싸는 부모 요소에게 `display: flex` 를 주어야한다.

## "가로 정렬? 세로 정렬?"

```css
.flexbox {
  display: flex;
  flex-direction: row; /* 가로 방향으로 정렬 */
  /* row | row-reverse | column | column-reverse */
}
```

- flex를 사용할 때, 보이지 않는 **2개의 축**이 생긴다
  - flex-direction에 따라서, flex의 **2개의 축**이 완전히 달라진다.

* 2개의 축 (`main axis`, `cross axis`)
  - `main axis`는 flex-direction의 방향에 따라서 결정된다.
  - `cross axis`는 main-axis의 수직 방향으로 결정된다.
    - cross-axis가 위에서 아래로 흐르는 이유는 `기본적으로 글을 읽는 순서`에 따르는 것!
  - ex) `flex-direction: row`
    - main axis ( ➡️ )
    - cross axis ( ⬇️ )
  * ex) `flex-direction: column`
    - main axis ( ⬇️ )
    - cross axis ( ➡️ )
  * ex) `flex-direction: row-reverse`
    - main axis ( ⬅️ )
    - cross axis ( ⬇️ )
  * ex) `flex-direction: column-reverse`
    - main axis ( ⬆️ )
    - cross axis ( ➡️ )

## "무조건 한 줄 안에 다 정렬?"

```css
.flexbox {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  /* nowrap | wrap */
}
```

- `flex-wrap: nowrap`
  - **감싸지 않고 자식의 사이즈를 줄여서라도** 한 줄로 정렬해버림
- `flex-wrap: wrap`
  - 한 줄에 모두 정렬하기에 공간이 넉넉하지 않으면, 여러 줄을 만들어버림
    - 자식 요소의 사이즈가 줄어들지 않는다.
