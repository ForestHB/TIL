## Mixin  
  - 프로젝트를 하다보면 밑줄임을 표현하는 스타일, 버튼 스타일, 아이콘 스타일에 해당하는 클래스를 만들어 놓고 필요한 위치에 클래스를 추가로 넣어주는 경우가 있는데, mixin 기능을 사용하면 더 쉽게 반복적인 작업을 할 수 있다. 또한 mixin은 특정 속성값을 인자로 전달할 수 있다.  
  mixin을 선언할 때는 @mixin 지시자를 사용하며, 적용할 때는 @include 지시자를 사용한다.  
  - SCSS  
    ```scss  
      @mixin ellipse-one($wid:100%){
        width: $wid;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
      }

      .text{
        @include ellipse-\one(80%);
      }
    ```  
  - css  
    ```css  
      .text {width: 80%; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
    ```  
  - 위 코드에서 ($wid:100%)는 $wid를 인자로 받는데 넘겨주는 것이 없을 경우 기본값을 100%로 전달한다는 것이다.  기본값은 콜론(:)값으로 정의한다. 그런데 주의해야 할 점은 기본값이 없는 인자에 대해 값을 넣어주지 않으면 에러가 난다는 것이다.  
