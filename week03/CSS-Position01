## Position

|값|의미|기준 요소 특징|
|:-:|:-:|:-:|
|Static|기본값|위치지정 불가(top,left 무시)|
|중요<br/>Relative|자기 자신을 기준으로 이동|자기자신 문서 흐름 유지, 위치만 이동|
|중요<br/>Absolute|가장 가까운 position 지정 조상 기준|부모 요소문서 흐름에서 제거됨|
|fixed|브라우저 창 기준 고정|viewport 스크롤에도 위치 공석|
|sticky|스크롤에 따라 relative>ficed 전환|부모요소 조건 만족 시 고정 (top등 지정 필요)|






### 01 Relative




##### html 구조
```html
<body>

    <div>1</div>
    <div>2</div>
    <div>3</div>
    <div>4</div>

</body>
```
<br/>
<br/>

##### 기본 스타일링
```css

        *{box-sizing: border-box;}
        body{margin: 0; padding: 0;}
        div{
            width: 50px;
            height: 50px;
            border: 1px solid;
            background-color: cornflowerblue;
        }


```

##### relative

```css
        div:nth-child(1){
            /* static은 위치이동 불가
            relative 이상부터 가능
            "static의 위치를 기준"으로 이동 */
            position: relative;
            left: 50px;
            top: 10px;
            /* right: 0;
            bottom: 0; */
            
        }

        div:nth-child(2){
            /* 음수값 적용 O */
            position: relative;
            left: -10px;
            top: -10px;
        }

        div:nth-child(3){
            position: relative;
            /* left:50% 를 하면 보더의 넓이 때문에 가운데로 가지 않는다
            calc함수로 정가운데로 위치
            - 양 옆에 공백이 있어야 한다 */
            left:calc(50vw - 25px);
            top: calc(25vh - 25px);

        }

        div:nth-child(4){
            position: absolute;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;
            margin: auto;
        }
        /* 중요한 것은 static위치가 기준 위치 */
```

- 중요한 것은 static위치를 기준 위치로 하는 것 
---

static : 위치이동 불가  
relative 이상부터 가능  
중요 ※ static 위치 기준으로 이동 ※

---
### 02 Absolute


##### html 구조
```html
<body>

    <div class="ancestor">
        <div class="parent">
            <div class="son">1</div>
            <div class="son">2</div>
            <div class="son">3</div>
            <div class="son">4</div>
        </div>
    </div>
    

</body>
```


<br/>
<hr/>
<br/>

```css
        div {
            border: 1px solid;
        }

        .ancestor{
            width : 750px;
            height : 750px;
            background-color: aquamarine;
            border : 1px solid;
            margin: 50px;
            position: relative;
        }
        .parent {
            width: 500px;
            height: 500px;
            background-color: royalblue;
            position: relative;
            margin: 50px;
        }

        .son {
            width: 50px;
            height: 50px;
            background-color: orange;
        }

        .son:nth-child(1){
            position: absolute;
            left: 0px;
            top: 0;
        }
```

absolute는 부모를 기준으로 이동  
부모의 포지션이 static일 경우 사위 요소를 기준으로 찾아간다.  
상위에도 없으면 가장 왼쪽 상단 기준
---
### 03 Global Navigation Bar

#### html 구조
```html
<body>
    <!-- 기본구조 -->
    <!-- .wrapper>header>.top-header+nav^main>section^footer -->
    
    <div class="wrapper">
        <header>
            <div class="top-header"></div>
            <nav>

                <!-- ul.main-menu>li*4>a[href="javascript:void(0)"]{$_MAINMENU}+ul.sub-menu>li*5>a[href="javascript:void(0)"]
                 ul태그 안에 메인메뉴4개 안에 a태그 +ul태그 안에 서브메뉴 5개 안에 a태그 ] -->
                <ul class="main-menu">
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
            <section></section>
        </main>
        <footer></footer>
    </div>

    
</body>
```

#### navi css
```css
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
```
<br/>
<br/>


```css
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
        }
        .wrapper>header>nav>ul.main-menu>li>ul.sub-menu>a{
            display: block;

        }
        .wrapper>header>nav>ul.main-menu>li:hover>.sub-menu{
            display: block;
        }
```
---
