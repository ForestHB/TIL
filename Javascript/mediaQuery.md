# 반응형    
  웹사이트는 다양한 해상도에 대응하는 것이 자연스럽고 이것을 반응형이라고 한다.  
  이 반응형은 매우 중요한데, 이것을 가능하게 하는 것이 css 미디어 쿼리이다. 이 미디어쿼리를 사용하면 다양한 크기의 디바이스에서 수많은 사용자에게 적절한 화면을 제공할 수 있다.  
  하지만 이런 css 미디어 쿼리에도 한계가 있는데, 그것이 자바스크립트 영역이다. 예를 들어 화면에 애니메이션 효과가 있는데 이 애니메이션 효과의 정도를 여러 해상도에 따라 다르게 해주고 싶을 경우에 css 만으로는 여러가지로 손이 많이 가게 된다.  
## matchMedia  
  matchMedia는 css의 미디어쿼리와 비슷한 역할을 하는 메서드이다.  
  ```js  
    let condition = window.matchMedia("(max-width: 768px)");
    function OK() {
      if(condition.matches) {
        alert("OK!");
      } else {
        alert("NO!");
      }
    }

    OK();
  ```  
  위의 코드는 해상도가 768px이하일 때 "OK!"라는 문자열의 창을 띄어주고 그 외에는 "NO!" 창을 띄어준다는 뜻이다.

## window.innerWidth  
  browser window 뷰포트의 넓이
