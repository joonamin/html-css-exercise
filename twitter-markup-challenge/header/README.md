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





### Main

<img src="https://raw.githubusercontent.com/joonamin/UpicImageRepo/master/uPic/Screenshot%202024-08-05%20at%201.06.00%E2%80%AFAM.png" alt="Screenshot 2024-08-05 at 1.06.00 AM" style="zoom:67%;" />



* 본문에 있어서 가장 핵심적인 역할을 하는 요소들이 모여있는 영역
  * 본격적인 내용의 시작을 알리기 위해 사용
  * sectioning elements가 아님!!!
* **하나의 html 문서 안에는 단 하나의 `<main>` 만 존재할 수 있다**
* `section`, `navigation`, `article`, `aside` 같은 sectioning elements 내부에서 사용될 수 없다.
  * `main`이 parent container로써, 이와 같은 요소들을 감싸는 역할
* header, main, footer가 병렬적으로 딱 떨어지는 구조를 지향하는 것이 좋긴 하지만, 디자인에 따라서 이런 구성은 달라질 수 있다.
