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

## "신나는 플렉스박스 파티 타임!"

- 이제 플렉스박스를 잘 사용하는 법만 남았다.
  - `어떤 기준으로 자식 요소들을 정렬할 것인가?`
    - **main axis 기준**: `justify-content`
    - **cross axis 기준**: `align-items` 또는 `align-content`

* 정렬을 한다?

  - 부모의 main-axis를 기준으로 컨텐츠를 밸런스 있게 배치하는 것
  - `justify-content`: `{center | flex-start | flex-end | space-around | space-between | space-evenly}`
    - space 계열은 `요소와 요소 사이의` 간격을 기준으로 배치하는 것이다!
    - 즉, cross axis를 기준으로 정렬하는 기능인 `align-items` 에서는 사용이 불가능한 값이다!!

* float에서는 center를 기준으로 배치하는 기능은 없지만, flexbox에서는 이를 제공한다.

  - 부모의 cross-axis를 기준으로 컨텐츠를 밸런스 있게 배치하는 것
    - 단, `wrap 속성에 따라` 다른 옵션이 적용된다.
      - `align-items`: cross-axis가 2개가 생기는 경우, 즉 wrap을 하여 자식 요소들을 다 포용하지 못하고 다음 flexbox까지 확장되었을 때, 각각의 cross-axis 축에 대해서 정렬을 수행
      - `align-content`: 전체 흐름에서의 cross-axis에 대해서 정렬을 수행하고 싶을 때
        - 이 경우는, 전체 흐름에서 cross-axis에 대해서 고려하는 것이기 때문에 `space-around`, `space-between` 과 같은 옵션도 작동한다.

  * 헷갈리면 기억하자!
    - 선 `align-items` 후 `align-content` (80% 정도 문제 해결 가능)

## order 측면

- flexbox를 활용하면 order 측면에서의 이점이 있다.
  - 만약, 사용하지 않고 순서를 고려해야한다면 마크업 과정이 매우 고단해질 것 이다.
  - flexbox의 자식요소에 `order` 를 지정해준다면 오름차순으로 요소가 플렉스박스 내부에서 배치될 것이다.
