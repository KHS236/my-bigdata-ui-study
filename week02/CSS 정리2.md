# BOX

- 목록
 - Margin
 - Padding
 - Border
 - Overflow

---

## Margin

```css
d1{
            /* all direction 동일 설정 */
            /* 전체방향 20px의 여백 */
            /* margin: 20px;*/

            /* 2개의 값으로 위top, 아래bottom,/ 좌left, 우right */
            /* margin: 20px 40px; */

            /* top:10px , right:20px , bottom:30px, left는 right와 동일 */
            /* margin: 10px 20px 30px; */

            /* top:10px , right:20px , bottom:30px , left:40px*/
            /* margin: 10px 20px 30px 40px; */
            
            margin-top:10px;
            margin-left:20px;
            margin-bottom:30px;
            margin-right : 40px;
```
Top 기준 --> 시계방향으로 left !


<br/>

로고를 가운데 맞추는 방법
```html

        /* 가운데 맞추기- 01 */
        .p1{
            position: relative;

        }
        .s1{
            position: absolute;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;
            margin: auto;
            /* 마진을 오토로 잡아주면 가운데로 고정된다 */

        }
```
포지션 일반적인 공식
상위는 relative
하위는 absolute
```html
        .p1{
            position: relative;

        }
        .s1{
            position: absolute;

        }
```


#### 방법2
```html

        /* 가운데 맞추기 - 02 */
        .p2{
            display: flex;
            justify-content: center; /*수평 배치 가운데*/
            align-items: center; /*수직 배치 가운데*/
        }

        /* 차이점
        1번은 자식과 상관없이 절대적인 위치를 가진다
        2번은 고정된 위치
        */
```

---

## Padding


```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            width: 200px;
            height: 200px;
            background-color: orange;
            border: 1px solid black;



        }
    </style>
</head>

<body>

    <div>HELLOWORLD</div>
</body>

</html>

```

- 마진과 같이 TOP>LEFT 시계방향으로 한 번에 설정할 수 있따.
- 전체 설정
  - padding : 10px;
- 위, 아래 / 좌 , 우
  - padding : 10px 20px;

- 위, 우, 하 / 좌는 우와 동일
  - padding : 10px 20px 30px;
- 위 우 하 좌
  - padding : 10px 20px 30px 40px;
  - padding-top:10px;
    padding-right:20px;
    padding-bottom:30px;
    padding-left:40px;

---

## Border

```css
        .d1{
            /* 보더 선 형태와 색 */
            border-top:2px solid red ;
            border-right: 3px dashed orange;
            border-bottom: 4px dotted blue;
            border-left:5px double green; 
        
        }
```
solid == 실선
dashed == 대쉬선
dotted == 도트점선
double == 기준선

---
#### 원 만들기
```html
        .d2{
            /* 보더 모서리 형태 */
            /* border-radius: 10px; 모서리 둥글게*/
            /* border-radius: 50%; 완전한 원*/

            /* 좌측 상단을 기준으로 Top > 시계방향 !*/
            /* 좌상,우하 / 우상 좌하 위치에 값 대입 */
            /* border-radius: 10px 50px; */

            /* 좌상/ 우상,좌하/ 우하 */
            border-radius: 10px 50px 80px;
```
-
radius를 이용해서 설정한 반지름을 가진 원모양으로 모서리를 둥글게 만든다.
50%를 지정하면 원모양이 나온다
---
#### 삼각형 만들기

```html
        .d3{
            /* 삼각형 만들기 */
            border-top:20px solid transparent;
            border-right:20px solid yellow;
            border-bottom:20px solid yellow;
            border-left:20px solid transparent;
            /* 상단 좌단을 투명하게 > 우단 하단 색깔 통일>wh 0 대입 (보더의 내용물 제거)*/

            width: 0;
            height: 0;
```
transparent == 보더 선 투명화


