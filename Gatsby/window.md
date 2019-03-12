# Gatsby window  
window는 componentDidMount() 내부에서만 사용해야 함 -> develop은 컴포넌트가 window가 정의된 브라우저에서 작동하지만(run) build의 경우, window가 정의되지 않은 서버에서 컴포넌트를 렌더링하기 때문.
