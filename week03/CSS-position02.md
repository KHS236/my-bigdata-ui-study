#### navi css 연습


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        /* common */
        *{box-sizing: border-box;}
        ul{padding: 0;margin: 0;list-style: none;}
        a{text-decoration: none;color: black;}
        body{margin: 0;padding: 0;}

        /* mainpage */

        /* 헤더 */
        .wrapper{}
        .wrapper>header{}
        .wrapper>header>.top-header{}
        .wrapper>header>nav{
            /* border: 1px solid; */
            height: 35px;
            border-bottom: 1px solid lightgray;
        }
        
        /* 네비 */
        .wrapper>header>nav>ul.main-menu{
            display: flex; /*수평 배치*/
            justify-content: center;
            /* align-items: center; */
            /* gap: 20px; */
            height: 100%;
            /* background-color: antiquewhite;  */
            margin: 250px 0px;
            /* padding: 0 300px; */
            /* border: 1px solid; */
        }
        .wrapper>header>nav>ul.main-menu>li{
            height: 100%;
            padding:0 15px;
            position: relative;
        }
        .wrapper>header>nav>ul.main-menu>li>a{
            display: block;
            height: 100%;
            line-height: 35px;
            color: black;
        }
        
        
        
        .wrapper>header>nav>ul.main-menu>li>ul.sub-menu{
            /* border: 1px solid; */
            width: 150px;
            height: auto;
            position: absolute;
            left: 20px;
            top: 35px;
            display: none;
            padding: 10px;
            border-right: 1px solid lightgray;
            border-left: 1px solid lightgray;
            border-bottom: 1px solid lightgray;
        }
        .wrapper>header>nav>ul.main-menu>li>ul.sub-menu>li{
            width: 200px;
            /* background-color:lightsteelblue; */
            height: 30px;
            line-height: 30px;
            padding: 0 ;


        }
        .wrapper>header>nav>ul.main-menu>li>ul.sub-menu>li>a{
            display: block;
        }
        .wrapper>header>nav>ul.main-menu>li:hover>.sub-menu{
            display: block;
        }

        /* 메인 */
        .wrapper>main{}
        .wrapper>main>section{}



        /* 푸터 */
        .wrapper>footer{}


        body{
            font-size: 12px;
        }
    </style>



</head>
<body>
    

    <div class="wrapper">
        <header>
            <div class="top-header"></div>
            <nav>
                <ul class="main-menu">
                    <li>
                        <a href="javascript:void(0)">ALL</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)">패키지</a></li>
                            <li><a href="javascript:void(0)">신발</a></li>
                            <li><a href="javascript:void(0)">의류</a></li>
                            <li><a href="javascript:void(0)">kids</a></li>
                            <li><a href="javascript:void(0)">용품</a></li>
                            <li><a href="javascript:void(0)">Collaboration</a></li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">BEST</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)">패키지</a></li>
                            <li><a href="javascript:void(0)">신발</a></li>
                            <li><a href="javascript:void(0)">의류</a></li>
                            <li><a href="javascript:void(0)">kids</a></li>
                            <li><a href="javascript:void(0)">용품</a></li>
                            <li><a href="javascript:void(0)">Collaboration</a></li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">충무공 이순신 시리즈</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)">패키지</a></li>
                            <li><a href="javascript:void(0)">신발</a></li>
                            <li><a href="javascript:void(0)">의류</a></li>
                            <li><a href="javascript:void(0)">모자</a></li>
                            <li><a href="javascript:void(0)">키즈</a></li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">꿈의신소재 그래핀원단</a>
                    </li>
                    <li>
                        <a href="javascript:void(0)">친환경 소로나 원단</a>
                    </li>
                    <li>
                        <a href="javascript:void(0)">라스트 사이즈</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)"></a>신발</li>
                            <li><a href="javascript:void(0)"></a>의류</li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">Package</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)"></a>hero 이순신</li>
                            <li><a href="javascript:void(0)"></a>hero 안중근</li>
                            <li><a href="javascript:void(0)"></a>독도 패키지</li>
                            <li><a href="javascript:void(0)"></a>광복 패키지</li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">신발</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)"></a>KR 시리즈</li>
                            <li><a href="javascript:void(0)"></a>하티 시리즈</li>
                            <li><a href="javascript:void(0)"></a>퀀텀 시리즈</li>
                            <li><a href="javascript:void(0)"></a>어반 시리즈</li>
                            <li><a href="javascript:void(0)"></a>로스터 시리즈</li>
                            <li><a href="javascript:void(0)"></a>슬리퍼</li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">의류</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)"></a>맨투맨/후드티/긴팔티</li>
                            <li><a href="javascript:void(0)"></a>티셔츠</li>
                            <li><a href="javascript:void(0)"></a>팬츠</li>
                            <li><a href="javascript:void(0)"></a>아우터</li>
                            <li><a href="javascript:void(0)"></a>모자</li>
                            <li><a href="javascript:void(0)"></a>양말</li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">Kids</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)"></a>상하복 세트</li>
                            <li><a href="javascript:void(0)"></a>후드티/맨투맨</li>
                            <li><a href="javascript:void(0)"></a>티셔츠</li>
                            <li><a href="javascript:void(0)"></a>실내복</li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">용품</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)"></a>독도수분초</li>
                            <li><a href="javascript:void(0)"></a>머그컵</li>
                            <li><a href="javascript:void(0)"></a>액세서리</li>
                            <li><a href="javascript:void(0)"></a>케이스</li>
                            <li><a href="javascript:void(0)"></a>문구</li>
                            <li><a href="javascript:void(0)"></a>가방</li>
                            <li><a href="javascript:void(0)"></a>반려용품</li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">마스크</a>
                    </li>
                    <li>
                        <a href="javascript:void(0)">Collaboration</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)"></a>영화[하얼빈]</li>
                            <li><a href="javascript:void(0)"></a>서로상점</li>
                            <li><a href="javascript:void(0)"></a>사토꼬레아</li>
                            <li><a href="javascript:void(0)"></a>검은사막</li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">반려용품 아울렛</a>
                    </li>
                </ul>


            </nav>
        </header>
        <main>
            <section></section>
        </main>
        <footer></footer>
    </div>


    
</body>
</html>

```
---
## Fixed


### 전체 코드
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <!-- Global Navigation Bar -->

    <style>
        /* common */
        *{box-sizing: border-box;}
        ul{padding: 0;margin: 0;list-style: none;}
        a{text-decoration: none;color: black;}
        body{margin: 0;padding: 0;}



        /* main page*/


        .layout-01{
            max-width: 1280px;
            margin: 0 auto;
        }
        .layout-02{
            margin: 0 18.75vw;
        }
        .layout-03{
            padding: 0 18.75vw;
        }

        .bedge-item {
            width: 150px;
            height: 200px;
            border: 1px solid;
            background-color: bisque;

            position: fixed;     /* ✅ 고정 위치 */
            right: 20px;         /* 화면 오른쪽에서 20px 떨어진 위치 */
            bottom: 100px;       /* 화면 아래에서 100px 떨어진 위치 */
        }


        /* header */
        .wrapper{}
        .wrapper>header{}
        .wrapper>header>.top-header{}
        .wrapper>header>nav{
            /* 여기서 height를 잡으면 서브메뉴 크기가 더 커질 때
            고정되기 때문에 나중에 height는 빼줘야한다. */
            /* border: 1px solid; */
            height: 50px;
        }

        /* navi menu */
        .wrapper>header>nav>ul.main-menu{
            display: flex; /* 수평 배치*/
            justify-content: space-between; /* 사이사이 간격 주기 */
            height: 100%;
            background-color: antiquewhite;
            /* height 100% > 상위 nav의 height를 따름 */
        }
        .wrapper>header>nav>ul.main-menu>li{
            /* border: 1px solid; */
            height: 100%;
            padding: 0 20px;
            background-color: deepskyblue;

            /* 중요!! */
            position: relative;

        }
        .wrapper>header>nav>ul.main-menu>li>a{
            display: block;
            /* li>a 태그 메인메뉴를 블럭으로 잡는다 */
            height: 100%;
            line-height: 50px;
            /* 부모의 height가 50px --> line-height 50px
            컨텐츠 가운데 배치*/
            color: white;
        }
        .wrapper>header>nav>ul.main-menu>li>ul.sub-menu{
            /* border: 1px solid; */
            width: 100%;
            height: 100%;
            /* background-color: brown; */
            /* 중요! */
            position: absolute;
            left: 0;
            top: 50px;

            display: none;
        }
        .wrapper>header>nav>ul.main-menu>li>ul.sub-menu>li{
            background-color: aquamarine;
            height: 40px;
            line-height: 40px;
            padding: 0;
            text-align: center;
        }
        .wrapper>header>nav>ul.main-menu>li>ul.sub-menu>a{
            display: block;

        }
        .wrapper>header>nav>ul.main-menu>li:hover>.sub-menu{
            display: block;
        }


        /* main */
        .wrapper>main{}
        .wrapper>main>section{
            height: 500px;
            
        }

        .wrapper>main>section:nth-child(1){background-color: rgb(128, 252, 128);}
        .wrapper>main>section:nth-child(2){background-color: rgb(183, 89, 250);}
        .wrapper>main>section:nth-child(3){background-color: mistyrose;}
        /* .wrapper>main>section:nth-child(4){background-color: mediumturquoise;} */
        /* footer */
        .wrapper>footer{}
    </style>






</head>
<body>
    <!-- 기본구조 -->
    <!-- .wrapper>header>.top-header+nav^main>section^footer -->
    
    <div class="wrapper">
        <header class="">
            <div class="top-header "></div>
            <nav>

                <!-- ul.main-menu>li*4>a[href="javascript:void(0)"]{$_MAINMENU}+ul.sub-menu>li*5>a[href="javascript:void(0)"]
                 ul태그 안에 메인메뉴4개 안에 a태그 +ul태그 안에 서브메뉴 5개 안에 a태그 ] -->
                <ul class="main-menu layout-03">
                    <li>
                        <a href="javascript:void(0)">1_MAINMENU</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)">1_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">2_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">3_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">4_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">5_SUBMENU</a></li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">2_MAINMENU</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)">1_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">2_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">3_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">4_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">5_SUBMENU</a></li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">3_MAINMENU</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)">1_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">2_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">3_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">4_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">5_SUBMENU</a></li>
                        </ul>
                    </li>
                    <li>
                        <a href="javascript:void(0)">4_MAINMENU</a>
                        <ul class="sub-menu">
                            <li><a href="javascript:void(0)">1_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">2_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">3_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">4_SUBMENU</a></li>
                            <li><a href="javascript:void(0)">5_SUBMENU</a></li>
                        </ul>
                    </li>
                </ul>

            </nav>
        </header>
        <main>
            <section class="layout-03"></section>
            <section class="layout-03"></section>
            <section class="layout-03"></section>
        </main>
        <footer></footer>
    </div>


    <div class="bedge-item"></div>
    
</body>
</html>
```

중요한 부분 ↓
```css
        .bedge-item {
            width: 150px;
            height: 200px;
            border: 1px solid;
            background-color: bisque;

            position: fixed;     /* 고정 위치 */
            right: 20px;         /* 화면 오른쪽에서 20px 떨어진 위치 */
            bottom: 100px;       /* 화면 아래에서 100px 떨어진 위치 */
        }

```



- position: fixed
  - 브라우저 화면을 기준으로 고정
  -  스크롤 했을 때 위치가 고정된다.
  - right,bottom의 값 + 뷰포트 기준으로 고정된다

 ---
 ## STICKY


#### 전체 코드
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        body{
            height : 3000px;
        }
        .wrapper>main>section {
            height: 500px;
        }
        .wrapper>main>section>.parent {
            width: 500px;
            height: 500px;
            background-color: royalblue;
            position: relative;
            display: flex;
            justify-content: space-between;
            align-items: start;
            margin-top:250px;
        }
        .wrapper>main>section>.parent>.son {
            width: 100px;
            height: 100px;
            background-color: orange;
            border: 1px solid;

            display:flex;
            justify-content: center;
            align-items: center;
        }

        /* relative */
        .wrapper>main>section>.parent>.son:nth-child(1){
            position:relative;
            left:0px;
            top:100px;
        }
        /* absolute */
        .wrapper>main>section>.parent>.son:nth-child(2){
            position:absolute;
            left:100px;
            top:0;
        }
        /* fixed */
        .wrapper>main>section>.parent>.son:nth-child(3){
            position:fixed;
            left:250px;
            top:250px;
        }
        /* sticky */
        .wrapper>main>section>.parent>.son:nth-child(4){
            position:sticky;
            left:0;
            top:0;
        }
        /* 부모영역 안에서만 스크롤에 따라 고정되어 움직인다 */







    </style>


</head>
<body>



    <div class="wrapper">
        <header>
            <div class="top-header"></div>
            <nav></nav>
        </header>
        <main>
            <section>
                <div class="parent">
                    <div class="son">relative</div>
                    <div class="son">absolute</div>
                    <div class="son">fixed</div>
                    <div class="son">sticky</div>
                </div>
            </section>
        </main>
        <footer></footer>
    </div>

    
</body>
</html>
```
평소에는 static처럼 동작한다.

스크롤이 특정 지점에 도달하면 fixed처럼 고정됨

※ 부모 요소의 범위 내에서만 고정된다. ※

---
## Zindex


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>


    <!-- zindex == 포지셔닝중 겹치는 부분이 생기면 어떤 녀석을 앞으로 보여줄지 설정 -->
    <style>


        /* position이 설정이 안되어있는 요소의 스타일엔 z-index 는 설정할 수 없다. */
        /* z-index : auto 순서에 맞게 z-index 를 고려  */
        .parent {
            width: 500px;
            height: 500px;
            background-color: royalblue;
        }

        .parent>.son {
            width: 100px;
            height: 100px;
            background-color: orange;
            border: 1px solid;
        }
        .parent>.son:nth-child(1){
            position: relative;
            top: 30px;
            left: 30px;
        }
        .parent>.son:nth-child(2){
            position: relative;
            z-index: 10;
        }
        /* zindex는 static에서 무시되기 때문에 최소한 포지션은
                relative이상 설정해줘야 한다 */


    </style>

</head>
<body>
        <div class="parent">
        <div class="son">1</div>
        <div class="son">2</div>
        <div class="son">3</div>
        <div class="son">4</div>
    </div>
</body>
</html>
```
- 개념  
  - 요소들이 겹칠 때 어떤 요소가 앞쪽에 보일지를 결정  
  - static에서 무시되기 때문에 최소한 포지션은 relative이상 설정해줘야 한다
