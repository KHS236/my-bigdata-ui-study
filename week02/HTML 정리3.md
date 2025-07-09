


## HTML CSS 연습 수업



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
            <input name="userid" type="text"/>
            <a class="btn" href="javascript:void(0)">중복확인</a>

        </div>
        <div class="row">
            <label>비밀번호</label>
            <input name="password" type="password"/>
            <!-- type="password" == 비밀번호 입력칸 가림 -->

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
        <!-- id = 유일한 값 / class = 묶는 거 / name = 여러개 -->
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
## 혼자 연습

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
                font-size: 0.9rem;
                box-sizing: border-box;
            }
            a{
                text-decoration: none;
                background-color: yellowgreen;
                color: rgb(89, 0, 255);
                border:1px solid;
            }
            body{
                margin: 0;
                padding: 0;
                
            }
            .btn{
                min-width: 80px;
                width: 80px;
                height: 100%;
                text-align: center;
                
                font-size: 0.9rem;
                line-height: 30px;
            }
            .btn-submit{
                width: 100%;
                background-color:yellowgreen;
                color: rgb(89, 0, 255);
                border:0;
            }
            form{
                background-color: rgb(255, 246, 233);
                width: 450px;
                border: 1px solid;
                margin: 40px auto;

        }
        form>.row{
            margin: 5px;/*행간 간격*/
            display:flex;/*수평배치를 기본으로*/
            justify-content: left;
            align-items: center;
            gap:5px;/*행 안의 간격 조절*/
            height:33px;

        }
        form>.row>label{
            display: block;
            min-width: 90px;
            height: 100%;
            line-height: 33px;
        }
        form>.row>input[type="text"],
        form>.row>input[type="password"]
        form>.row>select
        {
            height: 100%;
            width: 100%;
            outline:none;
            border-radius: 0;
            border: 1px solid gray;

        }
        .header>h2{
            width: 100%;
            text-align: left;
            font-size: 1rem;
            border-bottom: 1px solid lightgray;
            padding-bottom:5px;
        }
        .row>h6{

        }



    </style>

</head>
<body>

    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>


</head>
<body>
    
    <hr/>        
    <br/>
    <form action="/test.jsp" method="post">
        <div class="row header">
            <h2>회원 기본정보</h2>
        </div>
        <br/>
    <div class="row">
        <label for="">ID</label>
        <input name="userid" type="text">
        <a class="btn" href="javascript:void(0)">중복확인</a>

    </div>
    <div class="row">
        <label for="">비밀번호</label>
        <input name="password" type="password">

    </div>
    <div class="row">
        <label for="">비밀번호 확인</label>
        <input name="re-password" type="password">

    </div>
    <div class="row">
        <label for="">정보관리e-mail</label>
        <input name="inpo-mail" type="text">

    </div>
    <hr/>
    <div class="row header">
        <h2>회원 세부정보</h2>
    </div>
    <br/>
    <div class="row">
        <label for="">이름</label>
        <input name="username" type="text">
    </div>
    <div class="row">
        <label for="">전화번호</label>
        <input name="call" type="text">
    </div>
    <div class="row">
        <label for="">휴대폰</label>
        <input name="phone1" type="text">-
        <input name="phone2" type="text">-
        <input name="phone3" type="text">
    </div>
    <div class="row">
        <label for="">우편번호</label>
        <input name="zipnumber" type="text">
        <a class="btn" href="javascript:void(0)">찾기</a>
    </div>
    <div class="row">
        <label for="">주소</label>
        <input name="addr1" type="text">
    </div>
    <div class="row">
        <label for="">(상세 주소)</label>
        <input name="addr2" type="text">
    </div>
    <hr/>
    <div class="row header">
        <h2>가입경로 및 정보메일 수신여부</h2>
    </div>
    <br/>
    <div class="row"> 
        <label for="">가입 경로</label>
            <select>
                <option value="" selected>주위의 소개</option>
                <option>검색</option>
                <option>이것</option>
                <option>저것</option>
            </select>
    
    </div>
    <div class="row">
        <label for="">자동가입방지</label>
        <input name="protector" type="text">  159357
    </div>
    <div class="row">
        <label>메일 수신여부 </label>
    <div class="row">
        <h6>
            이벤트 및 서비스 관련 정보를 받기
        </h6>
    </div>
        <br/>
        <input name="smbirth" type="radio"/> 예
        <input name="smbirth" type="radio"/> 아니오
        <br/>
    </div>
    <div class="row">
        <h6>
            통큰아이 소식도 받아보시고 SMS서비스도 무료로 이용하세요.
        </h6>
    </div>
    <div class="row">
        <input class="btn btn-submit" type="submit" value="회원가입"/>        
    </div>
    </form>






    
</body>
</html>

</body>
</html>
```


##### css는 어렵다..

















