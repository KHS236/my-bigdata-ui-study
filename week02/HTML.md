

## HTML 개념

###### Hyper | Text | Markup | Language  의 약어  
웹문서 파일을 제작하는 언어  


## html 기본 구조

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <title>문서 제목</title>
  </head>
  <body>
    <h1>제목</h1>
    <p>문단 내용</p>
  </body>
</html>
```
---
<!DOCTYPE html> : HTML5 문서임을 선언
<html lang="ko"> :  페이지 언어를 한국어로 설정
<meta charset="UTF-8"> : 인코딩 설정
<title> : 브라우저 탭 제목
---

<시작>내용</종료>
##### ex) < head > < /head >

내용이 없으면 <태그 />  



head = 눈에 보이는 게 아니라 브라우저한테 지시하는 머리말


1. Block 태그 vs Inline 태그


```html
<body>
    <!-- 제목태그 h1~6 -->
    <h1>HELLO WORLD</h1>
    <h2>HELLO WORLD</h2>
    <h3>HELLO WORLD</h3>
    <h4>HELLO WORLD</h4>
    <h5>HELLO WORLD</h5>
    <h6>HELLO WORLD</h6>
</body>
```

### Block
- block은 줄바꿈이 자동, 너비/높이 지정 가능
- 개발자도구(f-12) elements로 찍어보기
- 하나의 행만 사용

### Line
- 내용만 감싸고 너비 높이 지정이 제한적임
- 같은 행을 공유

### < br/ >
줄바꿈


---
## Block / InLine
---
```html
    <h1>HTML</h1>
    HTML을 기술하기 위하여 사용하는 명령어의 집합을 태그(Tag)라고 한다.
    태그는 <p>기본적으로 여는 태그와 닫는 태그로 구성</p>되며,
    닫는 태그 없이 단독으로 이용하는 태그도 있다. 태그에 주는 다양한 옵션은
    모두 여는 태그에 지정하며, 닫는 태그는 태그 효과가 적용되는
    <div style="padding:20px; margin:20px; border:1px solid; width:200px; height:200px;">범위의 끝을 나타내는 기능만 한다.</div>
```
    < div style="padding:20px; margin:20px; border:1px solid; width:200px; height:200px;" >



```html
    그런데 태그 종류가 수십 가지가 넘는 데다,
    지정가능한 옵션까지 일일이 열거하면 책 한 권 분량이 된다.
    따라서 <span style="padding:20px; margin:20px; border:1px solid; width:200px; .height:200px;">일반인은 사용빈도가 높은 일부 태그만 암기하고,</span> 나머지는
    '태그사전(또는 레퍼런스)'이라고 하는
    도움말 파일을 참고하는 편이다. 물론 암기 범위는 고급 사용자 내지는
    프로페셔널(흔히 웹 퍼블리셔라고 하는 사람들)로 갈수록 넓어진다.
```
    < span style="padding:20px; margin:20px; border:1px solid; width:200px; height:200px;" >
---

## Block / InLine 차이점
```html
(Block)div >>
"padding:20px; - 박스 내부에 공간 > 박스가 커져서 다 뭉게진다
margin:20px; - 박스 외부 여백
border:1px solid; - 박스 만들기
width:200px;" - 너비 조절

(InLine)span >>
"padding:20px; - 내부 여백 행을 망가뜨리진 않는다
margin:20px; - 박스 외부 여백 행을 망가뜨리진 않는다
border:1px solid; - 박스 만들기
width:200px;" - 너비 조절
```

---

## list
```html
    <!-- ul-li : 순번 없는 리스트 -->
    <ul>
        <li>list01</li>
        <li>list02</li>
        <li>list03</li>
        <li>list04</li>
    </ul>

    <!-- ol - li : 순번 있는 리스트 (order) -->
    <ol>
        <li>list01</li>
        <li>list02</li>
        <li>list03</li>
        <li>list04</li>
    </ol>
```
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <ul>
        <li>
            2023학년도 수강과목
            <ol>
                <li>HTML/CSS/JS</li>
                <li>JQUERY</li>
                <li>REACT</li>
                <li>BOOTSTRAP</li>
            </ol>
        </li>
        <li>
            학년
            <ol type="A">
                <li>
                    1학년
                    <ul>
                        <li>HTML/CSS/JS/JQUERY</li>
                    </ul>
                </li>
                <li>
                    2학년
                    <ul>
                        <li>BootStrap / Clone Coding</li>
                    </ul>
                </li>
                <li>
                    3학년
                    <ul>
                        <li>React Redux</li>
                    </ul>
                </li>
                <li>
                    4학년
                    <ul>
                        <li>Type Script/Next.js</li>
                    </ul>
                </li>
            </ol>
        </li>
        <li>
            백엔드 언어
            <ol type="I">
                <li>JAVA</li>
                <li>JSP</li>
                <li>Servlet</li>
                <li>Spring</li>
                <li>Spring Boot</li>
            </ol>
        </li>
    </ul>


</body>
</html>
```
---
```html
	ul>li*4
```
### ul태그 안에 리스트 4개를 만듦.
---




## Class
#### 동일한 스타일링을 위한 틀
---

```html
<!-- 클래스 선택자 : '.' -->
     <!-- .c1 -->
    <div class="c1"></div>
    <div class="abc"></div>


    <!-- ID 선택자 : '#' -->
     <!-- #wrapper -->
     <div id="wrapper"></div>
     <span id="id2"></span>
    <span class="abc"></span>


    <!-- 속성 추가 : '[]' -->
    <!-- ol[type='I']>li*4{TEST $} -->
    <ol type="I">
        <li>TEST 1</li>
        <li>TEST 2</li>
        <li>TEST 3</li>
        <li>TEST 4</li>
    </ol>



    <!-- 템플릿 문서 구조 만들기 -->
    <!-- 기본 메인 구조 -->
    <!-- .wrapper>header>.top-header+nav^main>section*footer -->
    <div class="wrapper">
        <header>
            <div class="top-header"></div>
            <nav></nav>
        </header>
        <main>
            <section></section>
            <footer></footer>
        </main>
    </div>
```







---

### 단축키
- 복사 shift + alt + ↓
- 코드 정리 shift + alt + f

---
## Table

< table >
|태그|설명|
|-|-|
|<table>|표의 전체 틀|
|<tr>|테이블의 한 행(row)|
|<td>|일반 데이터 셀|
|th|제목 셀|
|thead|표의 머리글|
|tbody|표의 본문|
|tfoot|표의 바닥글|
|colspan|열 병합|
|rowspan|행 병합|



## 기본구조
```html
    table>tr*4>td*5
    <table>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
            <td></td>
        </tr>
    </table>

```



## ATag
###### 중요

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        body{height:3000px;}
        .btn{
            display:block;
            width:120px;
            height:30px;
            line-height:30px;
            text-align:center;
            text-decoration: none;
            margin:5px;
            border-radius: 10px;
            background-color: lightgray;
            font-size:.8rem;
            color: white;
            box-shadow: 3px 3px 3px lightgray;
            opacity: .8;
            transition: 1s;

        }
        .btn:hover{
            opacity: 1;
        }
        .btn-1{background-color: orange;}
        .btn-2{background-color: royalblue;}
        .btn-3{background-color: brown;}
        
    </style>
</head>
<body>
    


    <a class="btn btn-1" href="./02Basic">문서이동</a>
    <a class="btn btn-2" href="./03List"> 문서이동</a>
    <a class="btn btn-3" href="https://naver.com">NAVER</a>
    <hr/>

    <a href="https://daum.net/" target="frm1">DAUM으로 이동</a>
    <iframe src="" frameborder="1" width="400px" height="400px" name="frm1"></iframe>
        
        
        <!-- 인라인블럭
         라인안에 포함 돼 있으면서 크기가 조절됨 .  -->



    <!-- 기능이 없는 버튼을 만들면 가만히 두면 안 된다 -->
     <hr/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <br/>
     <a href="javascript:void(0)">기능1</a>
     <a href="javascript:void(0)">기능2</a>



</body>
</html>
```



## ATag2

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        header{
            position:fixed;
            right:0;
            top:0;
            border:2px solid;
            padding:10px;
            background-color: white;
        }

    </style>



</head>

<body>


    <!-- .wrapper>header+main>section*3>h2+p -->
    <div class="wrapper">
        <header>
            <a href="#html">HTML 이동</a>
            <a href="#css">CSS 이동</a>
            <a href="#js">JS 이동</a>
        </header>
        <main>
            <section>
                <a name="html"></a>
                <h2>HTML</h2>
                <p>
                    하이퍼본문표식달기언어는 웹 브라우저에 표시되도록 설계된 표준 마크업 언어다.
                    또한, HTML은 제목, 단락, 목록 등과 같은 본문을 위한 구조적 의미를
                    나타내는 것뿐만 아니라 링크, 인용과 그 밖의 항목으로 구조적 문서를 만들 수 있는 방법을 제공한다.
                    즉, 브라우저를 통해 화면에 '컨텐츠를 출력할 방법을 지정'한다. 그리고
                    이미지와 객체를 내장하여 대화형 양식을 생성하는 데 사용될 수 있다.
                    HTML은 웹 페이지 콘텐츠 안의 꺾쇠 괄호에 둘러싸인 "태그"로 되어있는 HTML 요소 형태로 작성한다.
                    HTML은 웹 브라우저와 같은 HTML 처리 장치의 행동에 영향을 주는 자바스크립트,
                    본문과 그 밖의 항목의 외관과 배치를 정의하는 CSS 같은 스크립트를 포함하거나 불러올 수 있다.
                    HTML과 CSS 표준의 공동 책임자인 W3C는 명확하고 표상적인 마크업을 위하여 CSS의 사용을 권장한다.
                </p>
            </section>
            <section>
                <a name="css"></a>
                <h2>CSS</h2>
                <p>종속형 시트 또는 캐스케이딩 스타일 시트(영어: Cascading Style Sheets)는 마크업 언어가 실제 표시되는 방법을 기술하는 스타일 언어(영어: style sheet
                    language or style language)로[1], HTML과 XHTML에 주로 쓰이며, XML에서도 사용할 수 있다. W3C의 표준이고, 페이지 레이아웃과 스타일을 정의할
                    때의 자유도가 높다. 기본 파일명[2]은 style.css이다.

                    마크업 언어(ex: HTML)가 웹사이트의 몸체를 담당한다면 CSS는 옷과 액세서리처럼 꾸미는 역할을 담당한다고 할 수 있다. 즉, HTML 구조는 그대로 두고 CSS 파일만
                    변경해도 전혀 다른 웹사이트처럼 꾸밀 수 있다.

                    현재 개발 중인 CSS3의 경우 그림자 효과, 그라데이션, 변형 등 그래픽 편집 프로그램으로 제작한 이미지를 대체할 수 있는 기능이 추가되었다. 또한 다양한 애니메이션 기능이
                    추가되어 어도비 플래시를 어느 정도 대체하고 있다.
                    CSS는 지속적으로 새로운 버전이 나오고 있다. 1996년에 도입된 CSS 1은 CSS의 바탕이 되었다. CSS의 표준으로는 CSS 2.1이 있으며 이전 버전에 비하여 새로운
                    기능과 도구가 추가되었다. 대다수의 웹 브라우저는 CSS 3를 잘 지원한다. 현재 W3C에서는 CSS 3를 표준으로 만들고 있다.

                    CSS는 여러 수준과 프로파일을 가지고 있다. 각 수준의 CSS는 일반적으로 새로운 기능을 담고 있으며 CSS1, CSS2, CSS3, CSS4로 나뉜다. 프로파일들은 일반적으로
                    특정한 장치나 사용자 인터페이스를 위해 만들어진 하나 이상 수준의 CSS의 하부 집합이다. 현재 휴대용 장치, 프린터, 텔레비전 수상기를 위한 프로파일들이 있다.
                </p>
            </section>
            <section>
                <a name="js"></a>
                <h2>JS</h2>
                <p>1993년, 일리노이 대학교 어배너-섐페인의 NCSA는 최초의 대중적인 그래픽 웹 브라우저인 NCSA 모자이크를 출시하였다. 1994년, 모자이크 커뮤니케이션스라는 이름의 회사가
                    캘래포니아주 마운틴 뷰에 설립되었으며 모자이크 넷스케이프를 만들기 위해 오리지널 NCSA 모자이크 개발자들을 고용하였다. 그러나 NCSA 모자이크와 코드는 의도적으로 공유하지
                    않았다. 이 기업의 브라우저의 내부 코드명은 모질라였으며 이는 "Mosaic and Godzilla"에서 비롯된 용어이다.[5]. 이 웹 브라우저의 첫 버전인 모자이크 넷스케이프
                    0.9는 1994년 말에 출시되었다. 4개월 후 브라우저 시장의 3/4를 잠식하면서 1990년대에 주된 웹 브라우저가 되었다. NCSA의 상표 소유권 문제를 회피하고자 이
                    브라우저는 같은 해에 "넷스케이프 내비게이터"로 이름을 바꾸었으며 이 기업은 "넷스케이프 커뮤니케이션스"라는 이름을 취하였다. 넷스케이프 커뮤니케이션스는 웹이 더 동적으로 변화할
                    필요가 있었음을 실감했다. 기업의 설립자 Marc Andreessen은 HTML에 코드를 웹 페이지 마크업으로 직접 작성하면서 웹 디자이너들과 파트타입 프로그래머들이 이미지,
                    플러그인 등의 요소를 쉽게 조합할 수 있는 글루 언어(glue language)가 필요했다고 믿었다. </p>
            </section>
        </main>
    </div>



</body>

</html>
```



#### 정리
##### HTML
- BLOCK(W:o,H:o,M:o,P:o)
- IN-LINE(W:x,H:x,M:△,P:△)
- ul-li
- table
- A tag
- Emmet











