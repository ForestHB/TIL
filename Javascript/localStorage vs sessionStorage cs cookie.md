# Storage, cookie  
## Storage  
  Storage는 web API로 cookie를 사용하는 것보다 좀 더 직관적으로 key/value 데이터를 안전하게 저장할 수 있는 메커니즘을 제공한다.  
  Storage 객체는 단순한 key-value 저장소이며 객체와 비슷하지만, 페이지 로딩에도 온전히 유지된다.  
  localStorage와 sessionStorage로 나뉜다.  
  - localStorage  
    - 저장하는 데이터에 만료기간이 없다.  
    - 오직 자바스크립트 또는 브라우저 캐시 / 로컬 데이터를 지우는 것으로만 제거할 수 있다.  
  - sesstionStorage  
    - 오직 하나의 세션에서만 데이터를 저장하는 객체이다.  
      - 하나의 세션에서만 유지되기 때문에 여러 페이지를 가지고있는 어플리케이션에는 사용하는 것이 부적절할 수 있다.  
    - 데이터는 서버로 전달되지 않는다.  

## cookie  
  
