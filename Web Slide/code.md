## 소스 코드  
  - webSlideShow.js  
    ```js  
      var imgArr = ["application-x-executable_36271.png", "Very-Basic-Folder-icon.png", "xxxCapt.jpg", "20180802_173709263.jpg", "beautifultSea.jpg"];  
      var btnArr = ["w3-button w3-display-left", "w3-button w3-display-right", "w3-button w3-change-BgColor", "w3-button w3-browser-new", "w3-button w3-Color-Link"];  
      var btnImgArr = ["Left", "Right", "Change", "New Page", "Color Code"];  
      var bgClr = ["Bisque", "DodgerBlue", "Khaki", "LightSteelBlue", "Aquamarine"];  
      var ttlTagName = 'h1';  
      var bgClrTagName = 'strong';  

      class webSlideShow {  
        constructor(){  
          var img_num = imgArr.length;  
          var button_num = btnArr.length;  
          var slide_Index = 0;  
          var body = document.getElementsByTagName('body');  
          body[0].bgColor = bgClr[slide_Index];  
          let webSlideShowReady = new image_Create(img_num, slide_Index);  
          let webSlideShowStart = new button_Create(button_num, img_num, slide_Index);  
        }
      }

      class image_Create{  
        constructor(img_num, body, slide_Index){  
          var img = document.createElement('img');  
          img.src = imgArr[i%img_num];  
          img.style.display = (i===slide_Index) ? "block" : "none";  
          body[0].appendChild(img);  
          body[0].getElementsByTagName(bgClrTagName)[0].innerHTML = "[ BackGround-Color : " + bgClr[slide_Index] +" ]";  
        }  
      }  

      class button_Create{
        constructor(button_num, img_num, body, slide_Index){
          for(let i = 0; i < button_num; i++){
            var mySlidesList = document.getElementsByTagName('img');
            var textVal = document.getElementsByName('new-color');
            var btn = document.createElement('button');
            btn.class = btnArr[i%button_num];
            btn.innerHTML = btnImgArr[i%button_num];  
            btn.addEventListener('click', function(event){  
              if(event.target.innerHTML === btnImgArr[2]){  
                let retVal = confirm(bgClr[slide_Index] + "를 " + textVal[0].value +"로 변경하시겠습니까?");  
                if(retVal === true){  
                  if(textVal[0].value == "") textVal[0].value = "white";  
                  bgClr[slide_Index%mySlidesList.length] = textVal[0].value;  
                  console.log("변경된 컬러 : " + textVal[0].value);  
                  textVal[0].value = "";  
                  body[0].getElementsByTagName(bgClrTagName)[0].innerHTML = "[ BackGround-Color : " + bgClr[slide_Index] +" ]";  
                  body[0].bgColor = bgClr[slide_Index%mySlidesList.length];  
                }  
              }  
              else if(event.target.innerHTML === btnImgArr[3]){  
                window.open("webSlideShow.html");  
              }
              else if(event.target.innerHTML === btnImgArr[4]){  
                window.open("http://www.homejjang.com/03/color_name.php");  
              }  
              else{  
                if(event.target.innerHTML === btnImgArr[0]) slide_Index--;  
                else if(event.target.innerHTML === btnImgArr[1]) slide_Index++;  
                if(slide_Index < 0) slide_Index += img_num;  
                for(let i = 0; i < img_num; i++){  
                  mySlidesList[i].style.display = "none";
                }  
                console.log(slide_Index%mySlidesList.length + 1 + "번째 그림");  
                mySlidesList[slide_Index%mySlidesList.length].style.display = "block";  
                body[0].bgColor = bgClr[slide_Index%mySlidesList.length];  
                body[0].getElementsByTagName(bgClrTagName)[0].innerHTML = "[ BackGround-Color : " + bgClr[slide_Index%mySlidesList.length] +" ]";  
              }
            });  
            body[0].appendChild(btn);  
          }  
        }  
      }  
    ```  

  - webSlideShow.html  
    ```html  
      <!DOCTYPE html>  
      <html>
        <head>
          <meta charset="UTF-8">
          <link rel="stylesheet" href="./webSlideShow.css">
          <script src="webSlideShow.js">
          </script>
          <h1> [ webSlideShow ] </h1>
          <strong> [ SlideShow ] </strong>  
        </head>
        <body>
          <section class="webSlideShow">
          </section>
          <script>
              let myWebSlideShow = new webSlideShow();
          </script>
          <form>
              Insert Color : <input type="text", name="new-color">  
          </form>
          <iframe src="https://html-color-codes.info/Korean/" longdesc="Color Code Search" frameborder=1></iframe>  
        </body>
      </html>  
    ```  

  - webSlideShow.js  
    ```css  
      img {
        width: 450px;
        max-width: 100%;
        height: 450px;
        max-height: 100%;
        margin: auto;
        display: "block";
      }  

      button {
        background: black;
        border: none;
        color: white;
        padding: 12px 25px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 10px;
      }

      iframe {
        width: 500px;
        max-width: 100%;
        height: 400px;
        max-height: 100%;
        margin: auto;
        align; middle;
      }
    ```  

## 학습 링크  
  - [[Html] div 컨테이너에 맞게 이미지의 크기를 자동 조정하는 방법](https://code.i-harness.com/ko/q/2e39ae)  
  - [[html/css]iframe](http://aboooks.tistory.com/205)  
