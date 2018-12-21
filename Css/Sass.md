## Sass  
  - 문법은 Sass와 SCSS가 있음.  
    - Sass는 들여쓰기 기반이므로 간편히 작성할 수 있고, 읽기 또한 쉬우나, CSS와의 호환성과 여러 줄 쓰기 지원 여부 등의 이율호 SCSS로 쓰기가 권장됨.  
  - 변수  
    - $ 로 시작할 수 있다. 변수 할당은 콜론(;)으로 마무리한다.  
    - 4가지 자료형을 지원한다.  
      - 수 (단위 포함)  
      - 문자열 (인용 부호가 있거나 없거나)  
      - 컬러 (하나 이상의 이름)  
      - 불리언 (boolean)  
  - 네스팅  
    - CSS눈 논리적인 네스팅을 지원하지만, 코드 블록 자체는 네스팅되지 않는다. Sass는 서로 간에 네스팅된 코드를 삽입할 수 있게 한다.  
  - 루프  
    - Sass는 @for, @each, @while를 사용하여 변수에 대한 루프를 지원하며, 비슷한 클래스나 id를 가진 요소들에 각기 다른 스타일을 적용하기 위해 사용할 수 있다.  
  - import  
    sass도 css처럼 import를 사용하여 여러 sass파일들을 import 할수 있다.  
      ```sass  
        @import "reset"
      ```
    - partial  
      만약에 .scss파일이나 .scss파일의 이름을 underscore로 시작하면 css파일로 따로 컴파일되지 않는다.  
  - extend  
    - Sass에서 특정 선택자를 상속할 때, @extend 지시자를 사용한다.  
    - SCSS  
      ```scss  
        .box {
          padding: 20px;
          border: 1px solid #333;
        }

        .news-box {
          @extend .box;
          background-color: #eee;
        }

        .list-box {
            @extend .box;
            background-color: #000;
        }
      ```  
