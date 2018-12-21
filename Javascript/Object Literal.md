# Object Literal  
    - Private methods  
      ```js  
        var Module = (function () {
            var privateMethod = function () {
               //do something
            };
        })();  
      ```  
    - Understanding "return"  
      ```  
        Typical Modules will use return and return an Object to the Module,  
        to which the methods bound to the Object will be accessible from the Module’s namespace.  
      ```  
      ```js  
        var Module = (function () {
          return {
            publicMethod: function () {
              // code
            }
          };
        })();  
      ```
      ```   
        As we’re returning an Object Literal, we can call them exactly like Object Literals:  
      ```  
      ```js  
        Module.publicMethod();  
      ```  
      ```  
        For those who haven’t used the Object Literal syntax before, a standard Object Literal  
        could look something like this:  
      ```  
      ```js  
        var myObjLiteral = {
          defaults: {name: 'LHB'},
          someMethod: function () {
            console.log(this.defaults);
          }
        };

        myObjLiteral.someMethod();
      ```  
      ```  
        But the issue with Object Literals is the pattern can be abused. Methods intended to be  
        “private” will be accessible by users because they are part of the Object. This is where  
        the Module comes in to save us, by allowing us to define all our “private” stuff locally   
        and only return “the good parts”.

        Let’s look at a more Object Literal syntax,  
        and a perfectly good Module Pattern and the return keyword’s role.  
        Usually a Module will return an Object, but how that Object is defined and constructed  
        is totally up to you. Depending on the project and the role/setup of the code,  
        I may use one of a few syntaxes.  
      ```  

      **Anonymous Object Literal return**  
        ```js  
          var Module = (function () {
            var privateMethod = function (){};
            return {
              publicMethodOne: function () {
                // I can call privateMethod() you know..
              }
              publicMethodTwo: function() {

              }
              publicMethodThree: function() {

              }
            };
          })();
        ```    

## 학습 링크  
  - [Mastering the Module Pattern](https://toddmotto.com/mastering-the-module-pattern/)  
  - [Web Worker](http://blog.302chanwoo.com/2016/08/webworker/)  
  - [3 ways to define a JavaScript class](http://steadypost.net/post/lecture/id/13/)  
  - [Object-Oriented ProgrammJavaScript](https://developer.mozilla.org/ko/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)  
