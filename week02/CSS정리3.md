




## 선택자 01


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        /* 전체 선택자 */
        /* 선택자 : * (바디 영역에 포함된 모든 태그) */
        *{
            box-sizing: border-box;
        }
        /* 요소 선택자 */
        /* 선택자 : 태그명 (각 태그 요소 선택) */
        div{
            width: 150px;
            height: 150px;
            border: 1px solid;
            margin: 10px;
        }
        /* id선택자 : # (유일한 요소 지정) 
        body 영역에 같은 id명으로 된 태그가 있으면 Js에서 문제가 생긴다.*/
        #id_01{
            background-color: rgb(79, 174, 107);
        }

        /* Class 선택자 : .클래스명 (특정 태그 그룹지정)*/
        .c1{
            background-color: blanchedalmond;
            color: red;

        }
        /* 그룹 선택자 : , (여러 선택자 지정) */

        #id_01,
        .c1{
            border-radius: 13px;
        }



    </style>




</head>
<body>


    <div class="c1"></div>
    <div id="id_01"></div>
    <div></div>
    <div class="c1"></div>
    <div>
        <p class="c1">HELLOWORLD</p>
    </div>


    <a class="btn btn--primary" href="./06.html">TESTA</a> 

    
</body>
</html>
```

---
### 전체 선택자 ( * )
- 바디를 포함한 바디 영역의 모든 요소 선택
<br/>
### 요소 선택자 (태그명)
- 특정 태그 이름으로 요소 선택
<br/>
### ID선택자 (#id)
- 태그 요소중 고유한 ID를 가진 요소 선택
- 같은 ID가 중복되면 JS에서 문제가 생길 수 있다
<br/>
### 클래스 선택자 (.Class명)
- 동일한 클래스 이름을 가진 요소들 선택
<br/>
### 그룹 선택자 ( , )
- 여러 요소를 같은 스타일로 적용시킬 때 복수 선택





---

## 선택자02

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        /* 자식 선택자 : >   */
        .parent>div{
            border: 1px solid;
            /* background-color: brown; */
        }
        .parent>p{
            color: orange;
        }
        .parent>.child{
            border-radius: 15px;
        }

        /* 자손 선택자 : 공백   */
        .parent p{
            background-color: red;
        }
        .parent div{
            font-size: 1.5rem;
        }

    </style>


</head>
<body>




    <div class="parent">
        <div class="child">
            <div>1 HELLOWORLD</div>
            <div>2 HELLOWORLD</div>
            <div>3 HELLOWORLD</div>
            <p>4 HELLOWORLD</p>
        </div>
        <div>5 HELLOWROLD</div>
        <p>6 HELLOWORLD</p>
    </div>


    <a class="btn btn--primary" href="./06.html">TESTA</a>

</body>
</html>
```
---

###  자식 선택자 (>)

- 특정 요소의 "직계 자식 요소"만 선택할 때 사용
- 바로 한 단계 아래의 요소만 적용됨
- 예: div > p  
  → div의 "바로 아래에 있는" p 태그만 선택

###  자손 선택자 (공백)

- 특정 요소의 "모든 하위 요소"를 선택할 때 사용
- 자식뿐 아니라, "모든 후손 요소" 에 적용 가능
- 예: div p  
  → div 안에 포함된 "모든 p 태그" 선택 (직계가 아니어도 됨)


  ---

  ## 기본 레이아웃 구조


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 공통영역common */
        *{}
        body{}
        ul{}
        a{}

        /* 레이아웃layout */
        .wrapper>header{}
        .wrapper>header>.top-header{}
        .wrapper>header>nav{}
        /* layout main */
        .wrapper>main{}
        .wrapper>main>section{}

        /* layout-footer */
        .wrapper>footer{}


    </style>


</head>
<body>

    <div class="wrapper">
        <header>
            <div class="top-header"></div>  <!-- 상단 헤더 (로고 등) -->
            <nav></nav>                      <!-- 내비게이션 -->
        </header>
        <main>
            <section></section>             <!-- 콘텐츠 섹션 -->
        </main>
        <footer></footer>                   <!-- 푸터 -->
    </div>

    <a class="btn btn--primary" href="./06.html">TESTA</a>

</body>
</html>
```
### 공통영역
* {}                  전체 요소 기본 스타일 초기화 
body {}               전체 바디 스타일 
ul {}                 리스트 초기화 또는 공통 스타일 
a {}                  링크 기본 스타일 

### 레이아웃 구조 정의
wrapper > header {}                         
- 헤더 전체 영역
<br/> 
.wrapper > header > .top-header {}
- 헤더 상단 영역 (로고, 유틸 등)
<br/>  
.wrapper > header > nav {}                  
- 네비게이션 영역

### 메인 콘텐츠 영역
.wrapper > main {}                          
- 메인 영역 전체
<br/> 
.wrapper > main > section {}                
- 개별 콘텐츠 섹션
<br/>

### 푸터 영역
.wrapper > footer {}                        
- 푸터 영역

---


## 선택자03

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        *{margin-left:30px;}
        .c1{border : 1px solid red;}
        .c2{border : 1px solid orange;}
        .c3{border : 1px solid green;}
        /*  
            ~ : 동위선택자(같은 Depth의 하위 모든 선택자)
            + : 동위선택자(같은 Depth의 하위 1개 선택자)
        */

        .c1>p{
            /* 자식 */
            color: blueviolet;
        }
        .c2~p{
            /* ~ 선택자는 해당(c2클래스)위치 위로는 보지 않는다 */
            /* 아래로 모든 형제 선택자 */
            background-color: orange;

        }
        .c2+p{
            /* 아래로 1개의 형제 선택자 */
            width: 200px;
        }
        .c2 p{
            /* 자손 */
        }

    </style>




</head>
<body>
<!-- 동위선택자 -->

    <div class="c1">
        <p>1 HELLO WORLD</p>
        <div class="c2">
            <p>2 HELLO WORLD</p>
            <div class="c3">
                <p>3 HELLO WORLD</p>
                <p>4 HELLO WORLD</p>
                <p>5 HELLO WORLD</p>
            </div>
            <p>6 HELLO WORLD</p>
            <p>7 HELLO WORLD</p>
        </div>
        <p>8 HELLO WORLD</p>
        <p>9 HELLO WORLD</p>
    </div>


        <a class="btn btn--primary" href="./06.html">TESTA</a>
</body>
</html>
```

### 형제 선택자
||선택자|설명|
|:-|:-:|:-|
|~|일반 형제 선택자|같은 부모를 가진 뒤에 나오는 형제 요소들 모두 선택|
|+|인접 형제 선택자|같은 부모를 가진 바로 다음 형제 요소 하나만 선택|


---


## 커스텀 체크박스

#### 기본 체크박스를 숨기고 사용자 정의 체크박스 구현



### html 구조
```html
    <div class="chk-block">
        <input type="checkbox" id="chk">
        <label class="check-label" for="chk"></label>
        <span>체크박스</span>
    </div>
    /* <input type="checkbox"> : 실제 체크박스 (보이지 않음)
    <label for="chk"> : 시각적으로 보이는 부분 (아이콘 포함)
    for="chk" 속성으로 label 클릭 시 checkbox가 토글됨 */
```








### CSS 스타일
```css

/* 모든 요소 box-sizing 설정 */
* {box-sizing: border-box;}

/* 체크박스 숨김 처리 */
input[type="checkbox"] {
    width: 150px;
    height: 150px;
    background-color: red;  /* 디버깅용 배경색 */
    display: none;
}

/* 라벨 기본 스타일 (체크 전 상태) */
input[type="checkbox"] + label {
    display: inline-block;
    width: 50px;
    height: 50px;
    border: 1px solid rgb(58, 252, 133);
    border-radius: 18px;

    background-color: rgb(125, 255, 175);
    background-image: url("./icon_off.svg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: 25px 25px;
}

/* 체크된 상태의 라벨 스타일 */
input[type="checkbox"]:checked + label {
    background-color: aquamarine;
    background-image: url("./icon_on.svg");
}

```
#### 요소선택자
- input[type="checkbox"]
  - 체크박스 인풋요소 전체
- input[type="checkbox"] + label
  - 체크박스 다음 label 선택
-  input[type="checkbox"]:checked + label
  - 체크된 상태에서의 label 스타일

---
#### css구조
display : none으로 기본 체크박스를 숨기고 label이 체크박스 역할을 한다  
이후 체크된 상태의 라벨 스타일 변경


---


## 버튼

```html
    <style>
        a{
            text-decoration: none;
            color:black;
        }
        .btn{
            display:block;
            width:130px;
            height:45px;
            line-height:45px;
            text-align:center;
            border-radius: 5px;
            color:white;
            font-weight:400;
            font-size:1.2rem;
            margin:5px;
            opacity:.7;

            transition: .2s;
        }
        .btn--primary{ background-color:royalblue}
        .btn--secondray{background-color: orange; }
        .btn--success{ background-color:blueviolet;}

        .btn:hover{
            opacity: 1;
            font-size:1.4rem;
        }
        .btn:active{
            color:gray;
            font-size : 1.2rem;
        }
        .btn:visited{
            color:black;
            background-color: tomato;
        }
    </style>
</head>
<body>
    
    <a class="btn btn--primary" href="./01.html">TESTA</a> 
    <a class="btn btn--secondary" href="./02.html">TESTB</a> 
    <a class="btn btn--success" href="./03.html">TESTC</a> 
    <a class="btn btn--success" href="./04Selector_동위.html">TESTD</a> 

</body>

```
#### 버튼을 눌러 페이지 이동
a태그를 버튼 형태로 디자인  
-> hover,active,visited 등 각 버튼 상태에 따라 다른 효과 적용
- ● hover
  - -마우스 포인터가 버튼 위에 올려졌을 때 적용
- ● active
  - -버튼을 클릭하는 동안 적용
- ● visited
  - -버튼을 사용하고 나면 적용
 
 
 ---



  ##  ::before, ::after 

```html

    <style>
        /* 
        ::before : content영역 앞에 표시할 스타일
        ::after : content영역 뒤에 표시할 스타일
        */
        div{
            width:400px;
            height : 200px;
            border : 1px solid;
            background-color: orange;
            text-align:center;
            line-height:200px;
        }
        .d1::before{
            content: '😜';

        }
        .d1::after{
            content: '😍';
        }
    </style>

</head>
<body>
    
    <div class="d1">
        HELLO WORLD
    </div>
</body>

```

|-|-|
|-|-|
|before|요소의 내용 "앞에" content 추가|
|after|요소의 내용 "뒤에" content 추가|

<br/>
😜HELLO WORLD😍
이런 식으로 출력된다 !

---

## 순서 기반 선택자

1. 리스트 항목 li 에 대해 짝수/홀수 줄마다 배경색을 다르게 지정
2. 첫 번째와 마지막 항목에만 별도의 width 적용





#### HTML구조

```html
<div>
    <ul>
        <li><a href="">TEST_1</a></li>
        <li><a href="">TEST_2</a></li>
        <li><a href="">TEST_3</a></li>
        <li><a href="">TEST_4</a></li>
        <li><a href="">TEST_5</a></li>
        <li><a href="">TEST_6</a></li>
        <li><a href="">TEST_7</a></li>
        <li><a href="">TEST_8</a></li>
    </ul>
</div>
```
아이템 총 8개, li에 다른 배경색과 너비 적용


---

#### CSS

```css
    <style>
        /* 기본 ul 스타일 초기화 */
        ul {
            list-style: none;
            margin: 0;
            padding: 0;
        }

        /* 모든 li에 공통 스타일 적용 */
        ul > li {
            width: 200px;
            height: 25px;
            border: 1px solid;
            margin: 10px;
        }

        /* 짝수 번째 li (2, 4, 6, 8) */
        ul > li:nth-child(2n) {
            background-color: aquamarine;
        }

        /* 홀수 번째 li (1, 3, 5, 7) */
        ul > li:nth-child(2n+1) {
            background-color: antiquewhite;
        }

        /* 첫 번째 li */
        ul > li:first-child {
            width: 500px;
        }

        /* 마지막 li */
        ul > li:last-child {
            width: 300px;
        }
        /* ※ nth-child()는 1부터 시작하는 인덱스 */

    </style>
```

|선택자|역할|
|-|-|
|ul > li:nth-child(2n)|2,4,6 ... 짝수 항목 선택|
|ul > li:nth-child(2n+1)|1,3,5 ... 홀수 항목 선택|
|ul > li:first-child|첫 번째 자식 요소만 선택|
|ul > li:last-child|마지막 자식 요소만 선택|


---
정리를 좀 더 세분화해서 했는데 더 깔끔하고 보기 좋아진 것 같다  
아직 깃허브에 정리하는 게 좋을지,노션 쓰는법을 배워야 하는지 잘 모르게따

