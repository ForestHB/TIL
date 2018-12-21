# css animation  
  - transform: translateX(), translateY(), translateZ()  
    - X, Y, Z축 기준으로 지정된 수치만큼 위치를 이동시키는 애니메이션 스타일 속성.  
  - animation-play-state: paused  
    - 해당 요소의 애니메이션 상태를 일시 정지 시키는 스타일 속성.  
  - [Scroll-Then-Fix Content][1]  
    - 화면이 스크롤된 후 특정 요소에 고정되는 스타일링.  
  - [Jquery ready()][2]  
    - DOM이 완전히 로드외었을 때 코드를 실행하도록 구현된 Jquery 메서드다.  
    - HTML document의 <body> tag 이하의 모든 엘리먼트가 로드가 된 후에 코드를 실행하게 되므로 <body> tag를 닫기 전에 스크립트 코드를 실행할 경우 ready() 메서드는 필요없다.  
    - 순수 자바스크립트에서는 DOMContentLoaded 이벤트를 대신 사용할 수 있다.  

[1]:https://css-tricks.com/scroll-fix-content/
[2]:https://github.com/codepink/codepink.github.com/wiki/%EC%88%9C%EC%88%98-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EB%A1%9C-%EC%A0%9C%EC%9D%B4%EC%BF%BC%EB%A6%AC-ready()-%EB%8C%80%EC%B2%B4%ED%95%98%EA%B8%B0
