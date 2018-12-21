# Open Graph Protocol  
  - sns 등에서 링크 공유 시 나타나는 미리보기 화면을 구성하는 메타 데이터 표기방법  
  - HTML 문서의 <head> 태그 내부에 <meta> 태그를 사용하여 작성  
  - 제목, 설명, 이미지 등으로 구성  
    - 제목  
    ```html  
      <meta property="og:title" content="제목">  
    ```  
    - 설명  
    ```html  
      <meta property="og:description" content="설명">  
    ```  
    - 이미지  
    ```html  
      <meta property="og:image" content="이미지 url">  
    ```  
  - 입력창에 입력된 문자열이 "링크"라는 것이 확인될 경우, 크롤러가 미리 그 링크의 웹사이트에 방문하여 head 태그 내부의 오픈그래프 메타데이터를 긁어와서 그것을 미리보기의 형태로 보여줌  
  - 오픈 그래프 메타데이터를 실제로 수정하여 적용시키더라도 캐싱 데이터에 의해 곧바로 적용되지 않을 수 있음  
  <hr>

# Link  
  - [링크의 미리보기 제목, 설명, 이미지를 결정하는 open graph 태그](http://blog.airbridge.io/open-graph-as-a-website-preview/)  
  - [Sharing Debugger](https://developers.facebook.com/tools/debug/sharing/)