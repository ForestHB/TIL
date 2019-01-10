# selector(선택)  
## Combinators and selector lists(결합자와 다중 선택자)  
### 결합자와 선택자 그룹  
  - Selector List  
    ```css  
      A, B {
        ...
      }
    ```  
    A또는 B 혹은 둘다 일치하는 요  
  - Descendant Combinators  
    ```css  
      A B {
        ...
      }
    ```  
    A와 일치하는 요소의 자손 중에 B와 일치하는 요소  
  - Child Combinators  
    ```css  
      A > B {
        ...
      }
    ```  
    A와 일치하는 요소의 자식 중에 B와 일치하는 요소  
  - Adjascent Sibling Combinators  
    ```css  
      A + B {
        ...
      }
    ```  
    A와 일치하는 요소의 다음 형제이면서 B와 일치하는 모든 요소
    즉, A와 같은 부모의 A 다음 자식  
  - General Sibling Combinators  
    ```css  
      A ~ B {
        ...
      }
    ```  
    A와 일치하는 요소의 다음 형제 중 하나면서 B와 일치하는 모든 요소  
    즉, A와 같은 부모의 다음 자식 중 일부
