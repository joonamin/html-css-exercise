# Media Query

- Responsive web을 구현하기 위해서 반드시 구현해야하는 것
  - responsive web?
    - 사용자가 접속한 브라우저에 반응하여 css를 입히는 기술

* 2가지 요건이 반드시 충족되어야한다.
  - html에서는 `viewport meta` 가 선언되어야하고
  - css에서는 `media query`가 선언되어야한다.

## `viewport meta` in html

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- viewport에 대해서 메타데이터를 추가하겠다.
        이 때 width 값은 device의 width값을 따른다.
     -->
    <meta name="viewport" content="width=device-width" />
    ...
  </head>
</html>
```

## `media query` in css

```css
/* 내가 보고 있는 화면의 사이즈가 768px 이상일 때, 아래 스타일을 적용  
    문법은 그대로 받아 들인다. `@media 쿼리를 screen에 대해서 적용할거야`
*/
@media screen and (min-width: 768px) {
  /* where all the magic happens */
}
```
