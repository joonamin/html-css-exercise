- 웹에서 가장 많이 사용자가 접하는 컨텐츠는 typography
  - 가독성있는 typography를 사용하면, 사용자에게 더 나은 경험을 제공할 수 있다.

* 아래 4가지에 대해서는 알아야한다.

  - line-height, letter-spacing, font-size, baseline

  * `line-height`

    - 줄 간격을 표현한다.
    - `px`, `em`, `rem` 을 단위로 줄 수 있다.
      - `em`을 많이 사용한다. 해당 폰트 사이즈와 비례하여 줄 간격을 먹일 것이다~
      - `line-height`를 표현할 때, `px` 과 `rem`은 단위를 표기해주는 것이 관례이지만, `em` 을 표기할 때는 단위를 생략하고 표기하는 것이 관례이다. (ex. `3em` = `3`)
      - **line-height값이 어떠하든, 글자는 줄 간격의 가장 가운대에 배치된다.**

  * `letter-spacing`

    - 글자와 글자 사이의 자간을 의미한다.
    - `px`, `em` 을 단위로 줄 수 있다.
      - `em`을 많이 사용한다. 해당 폰트 사이즈에 비례하여 표현하는 것이 자연스럽게 느껴지기 때문.
      - `em`을 생략하지 않고 표기한다!!

  * `font-size`

    - 글씨의 크기를 지정하는 것
    - `px`, `em`, `rem`
      - `px`는 절대 단위 (고정된 단위)
      - `em`, `rem` 은 상대 단위 (어떤 값을 기준으로 변하는 값)
        - `em`:= **"equal to capital M"** (실제로 적용된 폰트 사이즈)
        * ex) 자연스럽게 font-size가 20px로 적용될 경우, 1em은 20px이 된다.
        * `rem`:= **"root em"**
          - html 최상단의 요소 (`<html>`)의 `em`
          - html에 적용된 `font-size`를 1rem으로 삼는다.

  * `baseline`

    - 글자의 밑 받침이 되는 가상의 선

  * `font-family`

    - 서체를 표현할 때 사용
    - 사용하고자 하는 서체를 나열하는 것
    - 폰트 서체를 여러 개 나열 할 경우에는, 첫번째 서체를 적용하지 못한다면 두번째, 그것도 안된다면 3번째, ....

  - `font-weight`

    - font의 굵기를 표현하는데 사용한다 (100단위로 설정할 수 있다)
      - 100~900 까지의 숫자들 중, 100단위로 설정 (약속)
        - 400이 `regular size`, 700이 `bold size`
        - **수가 커질수록 bold체에 가깝다.**
        - **수가 작을수록 light체에 가깝다.**

  - `color`

    - font의 색깔을 표현하는데 사용한다.

    * 글씨에 사용하고싶은 색상을 선택하여 지정한다.
    * `hex`, `rgb`, `rgba` 를 사용하여 색상을 표현할 수 있다.
      - `#0066ff` => hex 방식
      - `rgb(0, 102, 255)` => rgb 방식
      - `rgba(0, 102 255, 1)` => rgba 방식 (마지막에 투명도가 추가된 것)

* minor
  - `text-align`
    - "텍스트를 정렬하는 기능"
      - `left | right | center`
  * `text-indent`
    - "들여쓰기를 할 때 그 크기를 명시하는 것"
      - -값도 사용이 가능하다.
  * `text-transform`
    - "텍스트가 변화한다는 뜻"
      - alphabetic한 문자들에게는 의미가 있다
        - `none | capitalize | uppercase | lowercase`
  * `text-decoration`
    - "텍스트를 어떤 방식으로 꾸밀 것인가?"
      - 거창한 것이 아닌, 텍스트에 줄을 긋는 것과 관련이 있음
    - `none | underline | line-through | overline`
    * anchor에 많이 사용된다.
      - anchor tag의 기본 스타일은 `text-decoration: underline` 이다. 이런 스타일이 마음이 안든다면 바꿀 수 있다.
  * `font-style`
    - `normal | italic | oblique`
    * `italic`체를 적용할 때 가장 많이 사용한다.
      - `<em>` 를 강조할 때 시맨틱 태그로 많이 사용.
        - 이 때, font-style은 기본적으로 italic으로 지정됨. 이를 재설정하고 싶을 때 사용!
