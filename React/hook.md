# useEffect
react Hook에서 추가된 class component의 lifecycle function을 대체할 수 있는 함수

```jsx
const YourFunctionalComponent = () => {
    useEffect(() => {
        ...
    }, deps);

    return (...);
}
```

deps는 의존성 값들의 배열로, useEffect는 이 배열 내부의 값이 변할 때만 재실행된다.

# useCallback
react Hook에서 추가된 function 최적화 함수

```jsx
const yourCallbackFunction = useCallback(() => {
    ...
}, deps);
```  

deps는 의존성 값들의 배열로, useCallback은 이 배열의 내부의 값이 변할 때만 재생성된다. 이 배열 값에 useCallback 내부에서 사용되는 함수를 추가할 경우, useCallback이 재생성되어도 해당 함수가 변하지 않으면 해당 함수를 다시 읽지 않으므로 최적화에 도움이 된다.  

# useState
react Hook에서 추가된, class component의 state를 대체할 함수

```jsx
const [value, setValue] = useState(defaultValue); // value = defaultValue
setValue(redefinedValue); // value = redefinedValue
```  