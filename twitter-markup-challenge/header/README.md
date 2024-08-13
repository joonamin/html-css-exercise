## Header

<img src="https://raw.githubusercontent.com/joonamin/UpicImageRepo/master/uPic/Screenshot%202024-08-05%20at%2012.17.28%E2%80%AFAM.png" alt="Screenshot 2024-08-05 at 12.17.28 AM" style="zoom:67%;" />





* 웹 페이지를 구성할 때, 최소한의 기능/의미를 갖는 단위로 쪼갰을 때 위 사진에 해당하는 영역은 `Header` 가 Sementic Tag로 적절해보인다.
  * 웹 페이지에 접속했을 때, 사용할 수 있는 기능들을 소개하는 영역들
  * 전체 페이지의 대제목을 표현하는 영역이기도 하다.
    * twitter 로고가 있다..!
* 의미론적으로 중요하게 사용하려면, 사용하고자 하는 `목적`이 분명해야한다.



### Navigation

* navigator들이 모여있는 공간들을 표현하는 section들이 존재
* sectioning elements 이므로, 반드시 heading이 존재





## Main

<img src="https://raw.githubusercontent.com/joonamin/UpicImageRepo/master/uPic/Screenshot%202024-08-05%20at%201.06.00%E2%80%AFAM.png" alt="Screenshot 2024-08-05 at 1.06.00 AM" style="zoom:67%;" />



* 본문에 있어서 가장 핵심적인 역할을 하는 요소들이 모여있는 영역
  * 본격적인 내용의 시작을 알리기 위해 사용
  * sectioning elements가 아님!!!
* **하나의 html 문서 안에는 단 하나의 `<main>` 만 존재할 수 있다**
* `section`, `navigation`, `article`, `aside` 같은 sectioning elements 내부에서 사용될 수 없다.
  * `main`이 parent container로써, 이와 같은 요소들을 감싸는 역할
* header, main, footer가 병렬적으로 딱 떨어지는 구조를 지향하는 것이 좋긴 하지만, 디자인에 따라서 이런 구성은 달라질 수 있다.





### Tweet Form 부분

<img src="https://raw.githubusercontent.com/joonamin/UpicImageRepo/master/uPic/Screenshot%202024-08-05%20at%201.08.52%E2%80%AFAM.png" alt="Screenshot 2024-08-05 at 1.08.52 AM" style="zoom:50%;" />

* 가장 만만하게 `논리적으로 완성된 집합체`를 표현하는 `<section>` sectioning element를 사용하자. 
* <u>remind</u>!! sectioning element는 항상 Heading이 필요하다.
  * CSS로 스타일링으로 안보이게끔 만들 수 있다.
  * Screen Reader로 들었을 때 정보의 명확성을 보장해야한다. 또한, 검색 엔진 최적화에도 큰 도움을 주기 때문이다.

* <u>remind</u>!! 내가 마크업하고자 하는 대상이 무슨 기능을 수행하고, 어떠한 태그로 표현할 수 있겠는지에 대한 고려만하자! 디자인은 나중에!



* 버튼들에 대한 고려
  * 첫 번째 버튼은 `<input>` 에 가까운 역할을 한다. 
    * input 태그는 스타일링이 진짜 안 먹는 요소이다.
    * <u>팁💡</u> 스타일링을 위해서 버튼을 대신해서 사용하고, js를 통해서 input으로 데이터를 입력받도록 유도하는 방식





### Timeline 부분

<img src="https://raw.githubusercontent.com/joonamin/UpicImageRepo/master/uPic/Screenshot%202024-08-05%20at%203.07.18%E2%80%AFAM.png" alt="Screenshot 2024-08-05 at 3.07.18 AM" style="zoom:50%;" />

* 논리적으로 완결된 하나의 기능들이 모여있음
  * 트윗들의 list 형식으로 보여주는 View
  * 보여지는 순서가 중요한 ordered list



#### Tweet 부분

> 실제 Timeline에 표현 될 list item

<img src="https://raw.githubusercontent.com/joonamin/UpicImageRepo/master/uPic/Screenshot%202024-08-05%20at%203.25.56%E2%80%AFAM.png" alt="Screenshot 2024-08-05 at 3.25.56 AM" style="zoom:50%;" />

* sectioning element인 `<article>` 을 사용해보자.
  * article: 정보 컨텐츠로서 의미의 완결성이 있는 컨텐츠 블록
    * section 보다는 하나의 완결된 정보 블록을 표현하는 것이므로 article이 좀 더 어울린다.
    * 독립적으로 존재하더라도 정보로서 의미가 있음



## Aside

<img src="https://raw.githubusercontent.com/joonamin/UpicImageRepo/master/uPic/Screenshot%202024-08-14%20at%201.01.14%E2%80%AFAM.png" alt="Screenshot 2024-08-14 at 1.01.14 AM" style="zoom:50%;" />

**논리적으로 완성이 되었지만, 본문과는 관련성이 떨어지는 내용들이 있는 구역**

* 본문의 내용과는 연관성이 떨어지는 부가 정보를 표현하기 위한 sectioning elements
* 물론 `<section>` 또한 의미의 완결성이 있으므로 채택해도 되지만, 전체 웹페이지에서는 `<aside>` 를 사용하는 것이 좀 더 의미론적으로 좋아보인다.
* 일반적으로 `사이드바`, `배너 광고`, `작은 위젯` 을 표현하는데 많이 활용된다.



## 마무리

* **결국, 웹 페이지를 마크업하기 위해서는 구획 나누기가 가장 중요하다**

  1. 의미를 담는 논리적인 집합체를 기준으로 구획을 설정한다

  2. 각각의 구획의 의미에 맞는 적절한 sectioning elements를 선정한다

     

* 구획을 나눈 다음, 각각의 컴포넌트들을 마크업하여 합치는 과정이다!

  * atomic design
