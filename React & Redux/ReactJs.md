## ReactJS  
  - Component LifeCycle : 컴포넌트가 "존재"하기 시작할  
    - render() -> componentWillMount() -> render() -> componentDidMount()  
  - Update  
    - componentWillReceiveProps() ->  
      shouldComponentUpdate()  == "true" ->  
      componentWillUpdate()  ->  
      render() ->  
      componentDidUpdate()  
  - State  
    - 리액트 컴포넌트 내부의 오브젝트의 state가 바뀔때마다 render() 발생  
    - ex  
      ```js  
        state = {
          greeting: 'hello'
        }

        render(){
          return({this.state.greeting})
        }
      ```  
