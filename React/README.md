## React  
### Rendering Elements
  - Rendering an Element into the DOM  
    ```js
      <div id="root"></div>
    ```  
    ReactDOM에 의해서 위의 div node 안의 모든 것이 관리되기 때문에 우리는 이것을 "root"라고 부른다. react에 의해 빌드된 App은 단순하게 하나의 root를 가지고 있다.만약, 이미 존재하는 app에 react를 합치려 한다면, 다음과 같이 ReactDOM.render()를 사용하면 된다.
    ```js
      const element = <h1>Hello, world</h1>;
      ReactDOM.render(element, document.getElementById('root'));
    ```  

    - Updating the Rendered Element  
    React element는 변경할 수 없다. 한번 하나의 element를 만들었다면, 그것의 자식이나 속성을 변경해서는 안된다. UI를 업데이트하는 유일한 방법은 새로운 element를 만들어서 ReactDOM.render()를 통해 전달하는 것이다.  

    - React Only Updates What's Necessary  
    React DOM은 element와 그 자식들을 이전 상태와 비교하고, Dom을 원하는 상태로 만드는 데 필요한 업데이트들을 적용한다.  

### Components and Props  
  - Function and Class Components  
    하나의 Component를 정의하는 가장 간단한 방법은 Javascript function을 사용하는 것이다.  
    ```js
      function Welcome(props) {
        return <h1>Hello, {props.name}</h1>;
      }
    ```  
    이 function은 하나의 props(properties)를 데이터와 함께 받아들이고 React element를 반환하기 때문에 유효한 React Component이다. 이러한 Component는 말그대로 Javascript function이므로 "function Components"라고 부른다.  
    또한 Component를 정의하는데 ES6 class를 사용할 수도 있다.  
    ```js
      class Welcome extends React.Component {
        render() {
          return <h1>Hello, {this.props.name}</h1>;
        }
      }
    ```   

  - Composing Components  
    Component들은 output에 다른 Component들을 붙일 수 있다. 이를 통해 모든 세부적인 수준에서 동일한 Components 추상화를 사용할 수 있다. 버튼, 폼, 대화 상자, 화면 등 React app에서 모든 것은 일반적으로 Component로 표현된다.
    ```js
      function Welcome(props) {
        return <h1>Hello, {props.name}</h1>;
      }

      function App() {
        return (
          <div>
            <Welcome name="Sara" />
            <Welcome name="Cahal" />
            <Welcome name="Edite" />
          </div>
        );
      }

      ReactDOM.render(<App />, document.getElementById('root'));
    ```

  - Props are Read-Only  
    Component를 function으로 선언하던지 Class로 선언하던지, 그것은 props를 절대로 수정하지 않는다.  
    ```js  
      function sum(a + b) {
        return a + b;
      }
    ```  
    위와 같은 function은 입력을 변경하려 하지 않고 항상 동일한 입력에 대해 동일한 결과를 반환하기 때문에 "pure"라고 한다.  
    대조적으로 다음의 function은 입력을 변경하기 때문에 "pure"하지 않다.  
    ```js
      function withdraw(account, amount) {
        account.total -= amount;
      }
    ```  
    모든 React Component들은 그것들의 props와 관련해서 "pure" function처럼 작동해야 한다.


## link  
  - [Functional setState is the future of React](https://www.vobour.com/%ED%95%A8%EC%88%98%ED%98%95-setstate%EA%B0%80-%EB%A6%AC%EC%95%A1%ED%8A%B8-react-%EC%9D%98-%EB%AF%B8%EB%9E%98%EC%9D%B4%EB%8B%A4-functiona)
