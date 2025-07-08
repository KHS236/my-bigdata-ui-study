

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


