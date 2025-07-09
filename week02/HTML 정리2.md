








## 이미지

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div style="width:250px; height:250px; border:2px solid;">
        
        <a href="https://naver.com" target="_blank">
            <!-- <img src="./10image.jpg" alt="짱구사진" /> --> <!-- 소스 : 이미지 경로 / alt : 이미지가 정상적으로 나오지 않을 때 출력할 문자열 메세지 -->
            <img style="width:100%;height:100%;"
            src="https://extmovie.com/files/attach/images/148/197/549/023/6d83b8645dfc575bf7e585e428a5cfeb.jpg" alt="짱구 사진" />
        </a>

    </div>
    
</body>
</html>
```



























## 비디오




```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style> /* <!-- 배경 화면 맞추기 - 왼쪽 상단 여백 제거--> */
        body{
            margin:0;
            padding:0; 
        }
        /* 바디영역 스크롤 제거 */
        body::-webkit-scrollbar{
            display:none;
        }
        .bg-video{
            position:absolute;
            left:0;
            top:0;
            width:100vw;
            height:100vh;
            z-index:-2;
            /* 뷰포트는 화면에 보이는 영역 100%로 맞추면 화면 크기에 따라 조절 */
        }
        .bg-video>video{
            width:100%;
            height:100%;
            object-fit:cover;
            /* 창을 줄여도 영상 크기를 창에 맞춤(여백 없앰) */
        }
        .gradient-overlay{
            position:absolute;
            left:0;
            top:0;
            height:30%;
            width:100%;
            /* background-color: orange; */
            /* background-origin: linear-gradient(방향top,botton,시작색상,종료색상); */
            background: linear-gradient(to bottom,rgba(0,0,0,0.8),rgba(0,0,0,0))
        }

    </style>

</head>
<body>

    <div class="wrapper">

        <div class="bg-video">
            <div class="gradient-overlay"></div> <!--비디오 태그 안에는 소스 태그 > 마임 타입-->
            <!-- < control autoplay muted loop> -->
            <video autoplay muted loop> <!-- 재생바(제거했음), 자동재생,
                                                    음소거(크롬 정책상 음소거시에만 자동재생이 가능하다., 반복재생)-->
                <source src="./11video01.mp4" type="video/mp4" art="배경" />
                <!-- 비디오 태그 안에는 소스 태그 > 마임 타입 -->
            </video>
        </div>

    </div>

    
</body>
</html>
```




## 비디오2


```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>


</head>

<body>
                                                <!--유튜브 도메인/정보를 제공하는 하위폴더~'?'' 까지 엔드포인트 > 'si'파라미터 = 인수 -->
                                                                                            <!-- 메서드 / 파라미터 = 값 /자동재생=1&음소거=1 -->
                                                <!-- "https://www.youtube.com/embed/mnbxbkuR51k?si=sBuN8UWsDCrqfNjw&autoplay=1&mute=1" -->
        <iframe width="560" height="315" src="https://www.youtube.com/embed/mnbxbkuR51k?si=sBuN8UWsDCrqfNjw&autoplay=1&mute=1"
        title="YouTube video player" frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>









</body>

</html>
```

	



## Form Tag

```html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>


<!-- 가장 중요 ! -->
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
         - PATCH            : 다음 시간에
         - DELETE           : 
         -->

    <form action="/test.jsp" method="post"> <!-- get : 기본값-->
        <div>
            <label>아이디</label>
            <input name="userid" type="text"/>
            <a href="javascript:void(0)">중복확인</a>

        </div>
        <div>
            <label>비밀번호</label>
            <input name="password" type="password"/>
            <!-- type="password" == 비밀번호 입력칸 가림 -->

        </div>
        <div>
            <label>비밀번호 확인</label>
            <input name="re-password" type="password"/>

        </div>
        <div>
            <label>이름</label>
            <input name="username" type="text"/>

        <div>
            <label>우편번호</label>
            <input name="zipcode" type="text"/>
            <a href="javascript:void(0)">검색</a>

        </div>
        <div>
            <label>기본주소</label>
            <input name="addr1" type="text"/>

        </div>
        <div>
            <label>상세주소</label>
            <input name="addr2" type="text"/>

        </div>
        <div>
            <label>휴대전화번호</label>
            <select>
                <option value="" selected>010</option>
                <option value="">011</option>
            </select>
            <input type="text"/>
            <input type="text"/>
            
        </div>
        <div>
            <label>연락처</label>
            <select>
                <option value="" selected>053</option>
                <option value="">055</option>
                <option value="">02</option>
            </select>
            <input type="text"/>
            <input type="text"/>
            
        </div>
        <div>
            <label>이메일</label>
            <input type="text"/>
            <select>
                <option value="" selected>.naver.com</option>
                <option value="">@outlook.co.kr</option>
                <option value="">@google.com</option>
            </select>
        </div>
        <div>
            <label>생년월일</label>
            <input name="smbirth" type="radio"/> 양
            <input name="smbirth" type="radio"/> 음
        </div>
        <div>
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
        <div>
            <input id="email-recv" type="checkbox"/> 
            <label for="email-recv">이메일 수신에 동의합니다.</label>
        </div>
        <!-- id = 유일한 값 / class = 묶는 거 / name = 여러개 -->
        <div>
            <input id="sms-recv" type="checkbox"/> 
            <label for="sms-recv">sms 수신에 동의합니다.</label>
        </div>
        <div>
            <input type="submit" value="회원가입"/>
            
        </div>
   
    </form>








</body>
</html>
```









### 연습

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>


</head>
<body>
    
    <hr/>        
    회원 기본정보
    <br/>
    <br/>
    <form action="/test.jsp" method="post">
    <div>
        <label for="">ID</label>
        <input name="userid" type="text">
        <a href="javascript:void(0)">중복확인</a>

    </div>
    <div>
        <label for="">비밀번호</label>
        <input name="password" type="password">

    </div>
    <div>
        <label for="">비밀번호 확인</label>
        <input name="re-password" type="password">

    </div>
    <div>
        <label for="">정보관리e-mail</label>
        <input name="inpo-mail" type="text">

    </div>
    <hr/>
    회원 세부정보
    <br/>
    <br/>
    <div>
        <label for="">이름</label>
        <input name="username" type="text">
    </div>
    <div>
        <label for="">전화번호</label>
        <input name="call1" type="text">
        <input name="call2" type="text">
        <input name="call3" type="text">
    </div>
    <div>
        <label for="">휴대폰</label>
        <input name="phone" type="text">
    </div>
    <div>
        <label for="">우편번호</label>
        <input name="call1" type="text">
        <input name="call2" type="text">
        <a href="javascript:void(0)">찾기</a>
    </div>
    <div>
        <label for="">주소</label>
        <input name="addr1" type="text">
    </div>
    <div>
        <label for="">(상세 주소)</label>
        <input name="addr2" type="text">
    </div>
    <hr/>
    가입경로 및 정보메일 수신여부
    <br/>
    <br/>
    <div> <label for="">가입 경로</label>
        <select>
            <option value="" selected>주위의 소개</option>
            <option>검색</option>
            <option>이것</option>
            <option>저것</option>
        </select>
    
    </div>
    <div>
        <label for="">자동회원가입방지</label>
        <input name="protector" type="text">  159357
    </div>
    <div>
        <label>메일 수신여부 | </label>
        이벤트 및 서비스 관련 정보를 받아보시겠습니까?
        <br/>
        <input name="smbirth" type="radio"/> 예 (무료문자 매일 5건 받기)
        <input name="smbirth" type="radio"/> 아니오
        <br/>
        통큰아이 소식도 받아보시고 SMS서비스도 무료로 이용하세요.
    </div>
    </form>






    
</body>
</html>
```








##### 연습 참조 사이트
```
https://www.tongkni.co.kr/support/sourcefile/090010010.html
```







