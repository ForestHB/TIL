# label  
  label 태그는 폼의 양식에 이름을 붙이는 태그다.  
## properties  
### for  
  같은 문서 내의 labelable 폼 관련 요소의 id를 참조하는 프로퍼티로, label 태그의 주요한 프로퍼티다.  
  ```html  
    <input type="radio" id="value1">
    <label for="value1">
  ```  
  위의 코드에서 label 태그의 for 프로퍼티 값으로 input 태그의 id 값을 주는 것으로 label 태그가 input 태그를 제어할 수 있게 된다.  

### form  
  폼을 소유하고 있는 라벨과 연관된 프로퍼티다.  
  지정된 속성 값은 <form>의 동일 도큐먼트 내 ID이다. 이것은 라벨 요소가 폼 요소에서 파생된 위치 뿐만 아니라 도큐먼트 내 어디에나 위치할 수 있게 한다.
