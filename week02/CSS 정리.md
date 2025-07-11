# CSS
###### 오늘 수업한 파일 저장을 잘못해서 내가 쓴 주석이 거의 다 날아갔다,,, 


## Block Vs Inline

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        div,span{
            border : 1px solid;
        }
        div{
            width : 300px;
            height : 200px;
            margin : 10px;
            /* top,right,left,bottom 상우하좌 시계방향*/ 
            padding : 20px;
            /* top,right,left,bottom */
            display:inline;
        }
        span{
            display:block;
            width : 300px;
            height : 200px;
            margin : 20px;
            padding : 20px;
        }
    </style>
</head>
<body>
    <!-- 
    블럭형태그(ex.div) : 하나의 라인전체를 사용하는 태그
    width,height,border,margin,padding : 적용가능
    인라인형태그(ex.span) : 한 라인안에 포함되어 있는 태그 
    width : x
    height : x
    border : o
    margin : left,right
    padding : o
    -->
    <div>HELLWORLD</div>
    <div>HELLWORLD</div>
    <hr>
    <span>HELLOWORLD</span>
    <span>HELLOWORLD</span>
</body>
</html>


```

---
## Style Priority

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    
  
    <style>
        h1{
            background-color: orange;
            color:white !important;
        }
    </style>
    <link rel="stylesheet" href="./css/common.css">

</head>
<body>
    
    <!-- 
        문서내 style 태그
        외부 css 생성 이후 link 설정(권장)
        inline style(권장 x)
        > 코드가 길어지면 한줄한줄 뜯어 고치기 힘들다
        !important(권장 x)
        > 코드가 길어지면 우선순위가 많이 꼬여서 고치기 힘들다
    -->

    <h1 style="background-color: red;color:black">HELLOWORLD</h1>
</body>
</html>
```
### css (모듈??이라고도 하나?)

```css
h1{
    background-color: royalblue;
    color:red;
}
```
#### css 생성해서 링크
```html
    <link rel="stylesheet" href="./css/common.css">
```
---

## Width Height
###### 내가 쓴 주석이 기억나지 않는다 내일 옆에 물어봐야겠따..

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .parent{
            width:100px;
            max-width:1280px;
            min-width:250px;
            /* height:300px; */
            min-height:400px;
            background-color: orange;
        }
        .son{
            width:150px;
            height:150px;
            background-color: royalblue;
        }
    </style>
</head>
<body>
    
    <!-- 
        width : auto(기본값 : 최대너비를 가지려는 성질)
        height : auto(기본값 : 최소높이를 가지려는 성질 )

        max-width   :   최대너비 
        min-width   :   최소너비
        max-height  :   최대높이
        min-height  :   최소높이
    -->
    <div class="parent">
        <div class="son"></div>
    </div>

</body>
</html>

```
---

##  Color

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        h1{color:cornflowerblue;}/*콘플라워 이름 예쁘다*/
        h2{color:rgb(255, 0, 0);}/* Red , Green , Blue*/
        h3{color:rgba(255,0,0,0.5)}/* Red , Green , Blue , alpha(투명도 0~1)*/
        h4{color:#FFFF00;}/*rgb코드는 8비트 16진수
                                rgb각각 0~255의 값을 가지고 16진수로 표현한다.*/
    </style>
</head>
<body>
    
    
    <h1>HELLO WORLD</h1>
    <h2>HELLO WORLD</h2>
    <h3>HELLO WORLD</h3>
    <h4>HELLO WORLD</h4>

</body>
</html>
```
---

## 단위
###### 양자역학은 기억나는데 주석이 기억나지 않는다,,

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{height:100px;margin:10px;background-color:orange;}
    </style>
</head>
<body>
    
    <!-- px : 고정크기 -->
    <div style="width:500px;">HELLO WORLD</div>
    <div style="width:500px;">
        <div style="width:300px;background-color:royalblue"></div>
    </div>
    <!-- % : 가변크기 , 상위태그(부모)를 기준 -->
    <div style="width:500px">
        <div style="width:50%;background-color:royalblue"></div>
    </div>
    <!-- vw,vh:가변크기 , 뷰포트를 기준 -->
         <div style="width:500px">
        <div style="width:50vw;background-color:royalblue"></div>
    </div>
</body>
</html>

```

### Background(배경이미지 지정)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{box-sizing:border-box;}
        body{margin:0;padding:0;}
        .wrapper{height:3000px;}
        .bg{
            position:absolute;
            top:500px;
            width:100%;
            height:400px;
            background-color:orange;
            /* 배경이미지 지정 */
            background-image:url('https://cdn.pixabay.com/photo/2025/06/28/17/56/forest-9685700_1280.jpg');
            /* 이미지 사이즈  cover : 전체 채우기  contain : 이미지 비율에 맞게 지정*/
           
            /* background-size:contain;
            background-repeat: no-repeat;
            background-position: center; */

            background-size: cover;
            background-attachment: fixed;
        }
    </style>
</head>
<body>
    

    <div class="wrapper">
        <div class="bg"></div>
    </div>

</body>
</html>
```
---
### Text

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <!-- 글자간격 -->
     <!-- 자간 많이 사용하지는 않는다 한 글자씩 간격 조절 -->
    <div style="letter-spacing:10px;">TEXT</div>
    <!-- 단어로 띄운다 띄어쓰기 기준? -->
    <div style="word-spacing:150px;">TEXT TEXT</div>

    <!-- 글자위치 -->
     <!-- line-height 200>> 상100 하100으로 height:200px;의 중간 지점 -->
    <div style="margin-bottom:20px;width:300px;height:200px;border:1px solid;text-align:center;line-height:200px;">TEXT</div>

    <!-- text-decoration -->
     <!-- 밑줄은 많이 쓸 것 같다 -->
    <div style="text-decoration:overline">TEXT</div>
    <div style="text-decoration:underline">TEXT</div>
    <div style="text-decoration:line-through">TEXT</div>
    <div>
        <a href="" style="text-decoration: none;">TEXT</a>
    </div>

    <!-- font-weight -->
     <div style="font-weight:100">HELLOWORLD</div>
     <div style="font-weight:200">HELLOWORLD</div>
     <div style="font-weight:300">HELLOWORLD</div>
     <div style="font-weight:400">HELLOWORLD</div>
     <div style="font-weight:500">HELLOWORLD</div>
     <div style="font-weight:600">HELLOWORLD</div>
     <div style="font-weight:700">HELLOWORLD</div>
     <div style="font-weight:800">HELLOWORLD</div>
     <div style="font-weight:900">HELLOWORLD</div>

    
</body>
</html>


```
---
## Font Size
###### width height style 그리고 이녀석이 중요한 것 같다.
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        :root {}
        /* rem을 사용하면 root로 기본값을 정의해주고 한 번에 컨트롤하기가 편해서 유지보수에 용이하다 */
    </style>
</head>

<body>

    <!-- px : 고정크기 기본값 : 16px-->
    <div style="font-size:24px;">
        <div style="font-size:32px">HELLOWORLD</div>
        <div style="font-size:100%">HELLOWORLD</div>
        <div style="font-size:8px">HELLOWORLD</div>
        <div style="font-size:16px">HELLOWORLD</div>
    </div>
    <hr />
    <!-- em : 상대크기(부모태그의 font-size를 기준 배수) -->
    <div style="font-size:24px;">
        <div style="font-size:2em">HELLOWORLD</div>
        <div style="font-size:48px">HELLOWORLD</div>
        <div style="font-size:0.5em">HELLOWORLD</div>
        <div style="font-size:12px">HELLOWORLD</div>
    </div>
    <hr />
    <!-- rem : 상대크기(기본글자크기(:root : 16px기준)) -->
    <div style="font-size:24px;">
        <div style="font-size:2rem;">HELLOWORLD</div>
        <div style="font-size:32px;">HELLOWORLD</div>
        <div style="font-size:.5rem">HELLOWORLD</div>
        <div style="font-size:8px">HELLOWORLD</div>
    </div>
    <hr />
    <!-- % : 상대크기 (상위태그 기준)-->
    <div style="font-size:24px;">
        <div style="font-size:100%">HELLOWORLD</div>
        <div style="font-size:50%">HELLOWORLD</div>
        <div style="font-size:200%">HELLOWORLD</div>
        <div style="font-size:75%;">HELLOWORLD</div>
    </div>
    <hr />
    <!-- vw : 상대크기(뷰포트를 기준) -->
    <div style="font-size:24px;">
        <div style="font-size:1vw;">HELLOWORLD</div>
        <div style="font-size:1.5vw">HELLOWORLD</div>
        <div style="font-size:2vw;">HELLOWORLD</div>
        <div style="font-size:clamp(16px,2vw,80px);">HELLOWORLD</div>
    </div>
    <hr />
    <!-- clamp(최소값, 기본값, 최댓값) -->
    <!-- vw :상대크기(뷰포트를 기준으로) -->
    <div style="width:90vw;height:200px;border:1px solid;margin:0 auto;">
        <div style="text-align:center;line-height:200px;font-size:clamp(1.5rem,5vw,6rem);">
            HELLOWORLD
        </div>
    </div>

</body>

</html>
```
---
## FontFamily


#### 글꼴 등록

##### 방법1
폰트 파일 경로를 link해서 불러올 수도 있으나
인터넷 연결이 계속 필요하다.

```html
    <!-- google font -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@200..700&display=swap" rel="stylesheet">
```



---
##### 방법2
글꼴 파일을 다운로드 받아서
@font-face를 이용해 폰트를 등록한다
```css
        /* 글꼴 등록 */
        @font-face {
            font-family: "custom01";
            src: url(./fonts/custom-font-01.ttf);
            font-style: normal;
        }

        @font-face {
            font-family: 'SkyblessingInjeFontTTF';
            src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/2507-1@1.0/SkyblessingInjeFontTTF.woff') format('woff');
            font-weight: normal;
            font-style: normal;
```
