# webfont

- 웹사이트에서 A라는 폰트를 사용하고 있는데, 해당 사용자의 컴퓨터에 해당 폰트가 없다면 기본 서체로 fallback되어서 디자인이 깨질 수 있다.

* 사용자에게 해당 폰트를 제공해주어야한다.
  1. 갖다 쓴다
  - 웹 폰트를 제공하는 사이트 (`font.google.com` 등의 웹 cdn을 이용)
  2. 직접 제공한다.
  - 나의 프로젝트 파일에 `assets` 폴더를 만들어서 제공하는 방식
  - css에 `@font-face { }` 를 지정
    - 이 때, `font-family`, `font-style`, `font-weight` 을 지정해준다
    - font-face에 spec을 기술하는 것이다.
      - 실제 폰트 source와의 매핑은 `src` 로 지정해준다.
      - url와 format 세트가 제공되는데, 브라우저 종류에 따라서 지원되는 폰트의 타입이 다를 수 있다. 효율적인 폰트 로딩을 위해서 사용
      * 외울 필요는 없다! 필요할 때 찾을 수 있도록~
  * **내가 만든 css 를 사용하기 위해서는**
    - `<link rel="stylesheet" href="./fonts.css"/>` 를 html에 지정
      또는
    - `@import url("./fonts.css")` 를 css에 지정
