## webpack  
  javascript 코드가 많아지면 하나의 파일로 관리하는데 한계가 있고,
  그렇다고 여러개의 파일을 브라우저에서 로딩하는 것은 그만큼 비효율적이다.  
  뿐만 아니라, 각 파일 내부의 변수들이 충돌할 위험성도 존재한다.  
  webpack은 이러한 문제점들을 보완하기 위해 파일 단위의 모듈 시스템을 하나의 파일로 묶어주는 모듈 번들러(module bundler)이다.

### Core Concepts  
  - Entry : module webpack이 내부 종속성 그래프를 작성하는 것을 시작하기 위해 무엇을 사용해야 하는가를 가리킴  
      ```js  
        module.export = {
          entry: './path/file.js'
        };  
      ```  
  - Output : 만들어진 번들을 방출하는 장소와 파일들의 이름을 지정하는 방법을 알려준다.  
      ```js  
        const path = require('path');

        module.export = {
          entry: './path/file.js',
          output: {
            path: path.resolve(__dirname, 'dist'),
            filename: 'my-first-webpack.bundle.js'
          }
        };  
      ```  
  - Loader : webpack은 JavaScript 파일만을 인식하지만, Loader는 webpack이 다른 타입의 파일을 가공하고 어플리케이션에 의해 사용될 수 있고 종속성 그래프에 추가될 수 있는 다양한 모듈을 변환해줌.  
      ```js  
        const path = require('path');

        module.export = {
          output: {
            filename: 'my-first-webpack.bundle.js'
          },
          module {
            rule: [
              { test: /\.txt$/, use:'raw-loader'}
            ]
          }
        };
      ```  
  - plugins : loader가 특정 타입의 모듈을 변환시키는데 사용되는데 반해, plugins은 번들의 최적화 등 더욱 넓은 범위의 업무를 수행하는데 사용된다.  
      ```js  
        const HtmlWebpackPlugin = require('html-webpack-plugin');

      ```  
      ```js  
        plugin: [
          new HtmlWebpackPlugin({template: './src/index.html'})
        ]  
      ```  

## Link  
  - [Webpack Concepts](https://webpack.js.org/concepts/)
