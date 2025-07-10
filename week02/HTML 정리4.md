





## CSS 복습




```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>

        /* common 영역 */
        *{/*전체 선택자*/
           font-size: 0.9rem; /*브라우저에서 제공하는 기본 폰트의 0.9%를 적용*/
           box-sizing: border-box; /*패딩이 늘어나도 전체크기 유지*/ 

        }
        a{/*a태그*/
            text-decoration: none; /*밑줄 제거*/
            color: black; /*글자 색*/
            border: 1px solid;

        }
        body{
            margin: 0;
            padding: 0; /*좌측 위 여백 제거*/
        }
        .btn{
            min-width:85px;
            height: 35px;
            line-height: 35px;
            border:1px solid gray;
            text-align: center;

        }
        .btn-submit{/* 회원가입 버튼은 개별처리 하고싶기 때문에 클래스화*/
            width: 100%;
            border: 0;/*테두리 제거*/
            color: white;/*글자 색상*/
            background-color: royalblue;/*버튼 배경색상*/
        }


        /* form 영역 */
        form{
            width: 370px; /*선택적이지만 모바일에서 잘 볼 수 있는 크기*/
            border: 1px solid; /*보더 박스*/
            margin: 50px auto; /* 위,아래 / 좌,우에 대한 여백 auto */
            /* padding: 5px; */

        }
        form>.row{/*클래스 명은 앞에 .*/
            margin: 10px;/*row(행)마다 간격*/
            height: 35px;
            display: flex;
            justify-content: left;/*수평 배치*/
            align-items: center;/*수직 배치*/
            gap: 5px;/*행 안의 아이템즈간 간격*/
        }
        form>.row>label{
            display: block;/*디스플레이를 블럭형으로 바꿔서*/
            min-width: 85px;/*라벨 최소 너비 조절*/
            border: 1px solid;/*각 라벨 보더*/
            height: 100%;/*부모가 가진 헤이트를 따름*/
            line-height: 35px;/* 부모 헤이트와 같이 */
        }
        form>.row>input[type ="text"],/* 인풋의 타입을 지정할 때 [] 사용 */
        form>.row>input[type="password"],/* 콤마를 사용해서 다른 타입 지정 */
        form>.row>select
        {
            width: 100%;
            height: 100%;

        }


    </style>


</head>
<body>


    <form action="/test.jsp" method="post">
        <div class="row">
            <h1>회원가입</h1>
        </div>
        <div class="row">
            <label>아이디</label>
            <input name="userid" type="text"/>
            <a class="btn" href="javascript:void(0)">중복확인</a>

        </div>
        <div class="row">
            <label>비밀번호</label>
            <input name="password" type="password"/>

        </div>
        <div class="row">
            <label>비밀번호 확인</label>
            <input name="re-password" type="password"/>

        </div>
        <div class="row">
            <label>이름</label>
            <input name="username" type="text"/>
        </div>
        <div class="row">
            <label>우편번호</label>
            <input name="zipcode" type="text"/>
            <a class="btn" href="javascript:void(0)">검색</a>

        </div>
        <div class="row">
            <label>기본주소</label>
            <input name="addr1" type="text"/>

        </div>
        <div class="row">
            <label>상세주소</label>
            <input name="addr2" type="text"/>

        </div>
        <div class="row">
            <label>휴대전화번호</label>
            <select>
                <option value="" selected>010</option>
                <option value="">011</option>
            </select>
            <input type="text"/>
            <input type="text"/>
            
        </div>
        <div class="row">
            <label>연락처</label>
            <select>
                <option value="" selected>053</option>
                <option value="">055</option>
                <option value="">02</option>
            </select>
            <input type="text"/>
            <input type="text"/>
            
        </div>
        <div class="row">
            <label>이메일</label>
            <input type="text"/>
            <select>
                <option value="" selected>.naver.com</option>
                <option value="">@outlook.co.kr</option>
                <option value="">@google.com</option>
            </select>
        </div>
        <div class="row">
            <label>생년월일</label>
            <input name="smbirth" type="radio"/> 양
            <input name="smbirth" type="radio"/> 음
        </div>
        <div class="row">
            <select>
                <option value="" selected>2025</option>
                <option value="">2024</option>
                <option value="">2023</option>
            </select>
            <select>
                <option value="" selected>12</option>
                <option value="">11</option>
                <option value="">10</option>
            </select>
            <select>
                <option value="" selected>09</option>
                <option value="">10</option>
                <option value="">11</option>
            </select>
        </div>
        <hr/>
        <div class="row">
            <input id="email-recv" type="checkbox"/> 
            <label for="email-recv">이메일 수신에 동의합니다.</label>
        </div>
        <div class="row">
            <input id="sms-recv" type="checkbox"/> 
            <label for="sms-recv">sms 수신에 동의합니다.</label>
        </div>
        <div class="row">
            <input class="btn btn-submit" type="submit" value="회원가입"/>
            
        </div>
   
    </form>








</body>
</html>
```

---
## 부트스트랩 연습


```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- BS5 -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM"
        crossorigin="anonymous"></script>



    <style>
        * {
            font-size: 0.9rem;
            box-sizing: border-box;

        }

        a {
            text-decoration: none;
            color: black;
            border: 1px solid;

        }

        body {
            margin: 0;
            padding: 0;
        }



        form {
            width: 370px;
            border: 1px solid;
            margin: 50px auto;


        }
    </style>


</head>

<body>


    <form action="/test.jsp" method="post">
        <div class="row m-2">
            <label class="col-3 form-label">아이디</label>
            <input class="col form-control" name="userid" type="text" />
            <a class="col-3 btn btn-danger ms-2" href="javascript:void(0)">중복확인</a>

        </div>
        <div class="row m-2">
            <label class="col-3 form-label">비밀번호</label>
            <input class="col form-control" name="password" type="password" />

        </div>
        <div class="row m-2">
            <label class="col-3 form-label">비밀번호 확인</label>
            <input class="col form-control" name="re-password" type="password" />

        </div>
        <div class="row m-2">
            <label class="col-3 form-label">이름</label>
            <input class="col form-control" name="username" type="text" />
        </div>
        <div class="row m-2">
            <label class="col-3 form-label">우편번호</label>
            <input class="col form-control" name="zipcode" type="text" />
            <a class="col-3 btn btn-light ms-2" href="javascript:void(0)">검색</a>

        </div>
        <div class="row m-2">
            <label class="col-3 form-label">기본주소</label>
            <input class="col form-control" name="addr1" type="text" />

        </div>
        <div class="row m-2">
            <label class="col-3 form-label">상세주소</label>
            <input class="col form-control" name="addr2" type="text" />

        </div>
        <div class="row m-2">
            <label class="col-3 form-label">휴대전화</label>
            <select class="col form-select">
                <option value="" selected>010</option>
                <option value="">011</option>
            </select>
            <input class="col form-control" type="text" />
            <input class="col form-control" type="text" />

        </div>
        <div class="row m-2">
            <label class="col-3 form-label">연락처</label>
            <select class="col form-select">
                <option value="" selected>053</option>
                <option value="">055</option>
                <option value="">02</option>
            </select>
            <input class="col form-control" type="text" />
            <input class="col form-control" type="text" />

        </div>
        <div class="row m-2">
            <label class="col-3 form-label">이메일</label>
            <input class="col form-control" type="text" />
            <select class="col form-select">
                <option value="" selected>.naver.com</option>
                <option value="">@outlook.co.kr</option>
                <option value="">@google.com</option>
            </select>
        </div>
        <div class="row m-2">
            <label class="col-3 form-label">생년월일</label>
            <input class="col-1 form-control form-check-input p-0 me-1" name="smbirth" type="radio" /> <label class="col-1 ps-0">양</label>
            <input class="col-1 form-control form-check-input p-0 me-1" name="smbirth" type="radio" /> <label class="col-1 ps-0">음</label>
        </div>
        <div class="row m-2">
            <select class="col form-select">
                <option value="" selected>2025</option>
                <option value="">2024</option>
                <option value="">2023</option>
            </select>
            <select class="col form-select">
                <option value="" selected>12</option>
                <option value="">11</option>
                <option value="">10</option>
            </select>
            <select class="col form-select">
                <option value="" selected>09</option>
                <option value="">10</option>
                <option value="">11</option>
            </select class="col">
        </div>
        <hr />
        <div class="row m-2">
            <input class="col-1 p-0 form-check-input " id="email-recv" type="checkbox" />
            <label class="col form-label" for="email-recv">이메일 수신에 동의합니다.</label>
        </div>
        <div class="row m-2">
            <input class="col-1 p-0 form-check-input" id="sms-recv" type="checkbox" />
            <label class="col form-label" for="sms-recv">sms 수신에 동의합니다.</label>
        </div>
        <div class="row m-2">
            <input class="col btn btn-primary " type="submit" value="회원가입" />

        </div>

    </form>








</body>

</html>
```

---
#### 유효성 체크 , 정규표현식



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        /* common */
        *{
            font-size: 0.9rem; /* 0.9배수 */
            box-sizing: border-box;
        }

        a{
            text-decoration: none;
            color: black;
            border: 1px solid;
            
        }

        body{
            margin: 0;
            padding: 0;
        }
        .btn{
            min-width: 80px;
            width: 80px; /*100% == 부모의 width 따름*/
            height: 100%;
            text-align: center;
            font-size: 0.8rem;
            line-height: 35px; /*row의 height 맞춰서*/

        }
        .btn-submit{
            width:100%;
            background-color: royalblue;
            color: white;
            border:0;
        }

        
        /* from */
        form{
            width: 370px;
            border:1px solid;
            margin: 50px auto;/*위쪽아래쪽*/
        }
        form>.row{
            margin: 10px;/*행간 간격*/
            display:flex;/*수평배치를 기본으로*/
            justify-content: left;
            align-items: center;
            gap:5px;/*행 안의 간격 조절*/
            height:35px;
            
        }
        form>.row>label{
            display:block;
            min-width: 85px; /*최소 85픽셀 너비*/
            height: 100%; /*수직 배치*/
            line-height: 35px; /* height와 같은 값 세트로 입력 가운데로 맞추기*/
            /* border : 1px solid; */
            
        }
        form>.row>input[type="text"],
        form>.row>input[type="password"],
        form>.row>select
        {
            height: 100%;
            width: 100%;
            outline:none;
            border-radius: 0;
            border:1px solid gray;
            
        }
        .top-header{
            height: 15px !important;
            background-color: black;
            
        }
        .title{
            margin-bottom:20px !important;
            
            
        }
        .title>h2{
            width: 100%;
            text-align: center;
            font-size: 2rem;
            border-bottom: 1px solid lightgray;
            padding-bottom:5px;
            

        }
        /*
        id      : 유일한 값을 가지는 식별자
        class   : 
        name    : 유일한 값 , 서버에 전달할 이름
        */
        </style>


</head>
<body>
    <!-- 1. <form> 태그란?
        사용자로부터 입력을 받아 서버로 전송하는 폼을 정의하는 태그
내부에 다양한 입력 요소 (input, textarea, select, button 등)를 포함 -->


    <!-- form   : 사용자로부터 특정 정보를 받아 서버로 전달하는데 사용되는 태그
         action Attribute   : 전달받는 서버 URI
         method Attribute   : 서버로 요청하는 방식
         - GET              : 사용자 요청 정보를 Query String으로 전달(Default)
         - POST             : 사용자 요청 정보를 Request body(Payload)로 전달
        ========================================================================
         - PUT              : 
         - PATCH            : 
         - DELETE           : 
         -->

    <form action="/test.jsp" method="post"> <!-- get : 기본값-->
        <div class="row top-header">

        </div>
        <div class="row title">
            <h2>회원가입</h2>
        </div>
        <div class="row">
            <label>아이디</label>
            <input
            name="userid"
            type="text"
            placeholder="아이디를 입력하세요"
            required
            />       <!--placeholder(입력하세요 ), required 유효성 체크 (입력 안 되면 안 넘어감)-->
            <a class="btn" href="javascript:void(0)">중복확인</a>

        </div>
        <div class="row">
            <label>비밀번호</label>
            <input
            name="password"
            type="password"
            pattern="^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[\W_]).{8,20}$"
            oninvalid="this.setCustomValidity('최소8자 및 최대20자, 하나 이상의 대문자 + 하나의 소문자 + 하나의 숫자+하나의 특수문자')"
            required
            />
            <!-- 정규표현식 ^ == 시작 , $ == 끝 , ?=. == 전방 탐색 , [] == 조건식
            ^(?=.*[a-z])a-z소문자,(?=.*[A-Z])A-Z대문자,(?=.*\d)숫자,(?=.*[\W_]).{8,20} -->
            <!-- aA!111 -->
            <!-- type="password" == 비밀번호 입력칸 가림 -->

        </div>
        <div class="row">
            <label>비밀번호 확인</label>
            <!-- disabled : 데이터가 서버로 전송되지 않음 , 입력불가
                 readonly : 데이터가 서버로 전송됨 , 입력 불가
            -->
            <input name="re-password" type="password" value="1234" readonly/>

        </div>
        <div class="row">
            <label>이름</label>
            <input name="username" type="text"/>
        </div>
        <div class="row">
            <label>우편번호</label>
            <input name="zipcode" type="text"/>
            <a class="btn" href="javascript:void(0)">검색</a>

        </div>
        <div class="row">
            <label>기본주소</label>
            <input name="addr1" type="text"/>

        </div>
        <div class="row">
            <label>상세주소</label>
            <input name="addr2" type="text"/>

        </div>
        <div class="row">
            <label>휴대전화</label>
            <select>
                <option value="" selected>010</option>
                <option value="">011</option>
            </select>
            <!-- 정규표현식 pattern="[0부터9까지 문자열]{3자리,4자리}" -->
            <!-- oninvalid="this.setCustomValidity('오류메세지')" -->
            <input type="text"
            pattern="[0-9]{3,4}" 
            oninvalid="this.setCustomValidity('0-9까지의 숫자만 입력해야합니다')"
            />
            <input type="text"/>
            
        </div>
        <div class="row">
            <label>연락처</label>
            <select>
                <option value="" selected>053</option>
                <option value="">055</option>
                <option value="">02</option>
            </select>
            <input type="text"/>
            <input type="text"/>
            
        </div>
        <div class="row">
            <label>이메일</label>
            <input type="text"/>
            <select>
                <option value="" selected>.naver.com</option>
                <option value="">@outlook.co.kr</option>
                <option value="">@google.com</option>
            </select>
        </div>
        <div class="row">
            <label>이메일2</label>
            <input type="email"/>
            <!-- email타입도 있따 -->
        </div>
        <div class="row">
            <label>생년월일</label>
            <input name="smbirth" type="radio"/> 양
            <input name="smbirth" type="radio"/> 음
        </div>
        <div class="row">
            <select>
                <option value="" selected>2025</option>
                <option value="">2024</option>
                <option value="">2023</option>
            </select>
            <select>
                <option value="" selected>12</option>
                <option value="">11</option>
                <option value="">10</option>
            </select>
            <select>
                <option value="" selected>09</option>
                <option value="">10</option>
                <option value="">11</option>
            </select>
        </div>
        <hr/>
        <div class="row">
            <input id="email-recv" type="checkbox"/> 
            <label for="email-recv">이메일 수신에 동의합니다.</label>
        </div>
        <!-- id = 유일한 값 / class = 묶는 거 / name = 여러개 -->
        <div class="row">
            <input id="sms-recv" type="checkbox"/> 
            <label for="sms-recv">sms 수신에 동의합니다.</label>
        </div>
        <div class="row">
            <input class="btn btn-submit" type="submit" value="회원가입"/>
            
        </div>
   
    </form>

## DATASET


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

    <div data-username="user1234" data-a="AAA">계정명</div>
    <div data-address="대구">주소</div>
    <div data-phone="01022223333">연락처</div>

    <script>
        const Els = document.querySelectorAll('div');
        Els.forEach(el=>{console.log(el.dataset)})
    </script>
</body>
</html>


```






</body>
</html>
```
