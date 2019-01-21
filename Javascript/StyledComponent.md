# styled-component  
  styled-component란 리액트 컴포넌트를 스타일링 해주는 css 코드를 보다 향상시켜주기 위한 것으로, 컴포넌트에 css 코드가 내장되어 있다로 볼 수 있다.  
  styled-component는 기존에 이곳저곳에 퍼져있던 css 코드들을 한 곳으로 모아주고, css 코드의 수정 및 삭제가 용이하며, 클래스 네임을 중복하여 사용하거나 오타가 나서 생기는 버그들을 신경쓰지 않아도 되는 등 굉장히 편리한 특성들을 가지고 있다.

## Usage  
### Getting Started  
  styled-component는 컴포넌트와 스타일 코드 간의 거리를 없에준다. 어떤 컴포넌트에 대해 스타일을 정의할때, styled-component는 그 컴포넌트를 생성하는 것과 스타일을 정의하는 것을 동시에 한다.  
  ```js  
    // styled-componet 임포트
    import styled from 'styled-components'

    // 스타일이 정의된 h1 태그를 렌더링하는 Title 컴포넌트
    const Title = styled.h1`
      font-size: 1.5em;
      text-align: center;
      color: palevioletred;
    `;

    // 스타일이 정의된 section 태그를 렌더링하는 Wrapper 컴포넌트
    const Wrapper = styled.section`
      padding: 4em;
      background: papayawhip;
    `;

    // 리액트 컴포넌트에서 styled-componet 사용
    render(
      <Wrapper>
        <Title>
          Hello World!
        </Title>
      </Wrapper>
    );
  ```  
  - props  
  컴포넌트에 전달될 프로퍼티에 따라 스타일을 줄 수도 있다.  
  ```js  
    const Button = styled.button`
      font-size: 10px;
      color: ${props => props.primary ? "red" : "blue"};
      border-radius: ${props => props.primary ? "30px" : "3px"};
      background: transparent;
    `;

    render(
      <div>
        <Button>Normal</Button>
        <Button primary></Button>
      </div>
    );
  ```  
  Button 컴포넌트에 "primary"라는 프로퍼티를 주는 것으로 그 Button은 color와 border-radius 속성으로 "red"와 "30px"이라는 값을 가지게 된다.  

  - extending styles  
    스타일을 상속하는 것도 가능하다.  
    ```js  
      const Tilte = styled.h1`
        color: palevioletred;
        background: lightgray;
        border: 2px solid black;
        border-radius: 3px;
        padding: 2rem;
      `;

      const tomatoTitle = styled(Title)`
        color: tomato;
        border-color: tomato;
      `;
    ```  
    tomatoTitle 컴포넌트는 Title 컴포넌트의 스타일을 상속받는다. tomatoTitle 컴포넌트 내부에서 재정의된 속성인 color와 border-color를 제외한 모든 스타일이 Title 컴포넌트와 동일하다.
