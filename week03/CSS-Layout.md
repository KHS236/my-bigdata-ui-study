## FLEX 01

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
        }

        .wrapper {
            width: 1280px;
            height: 1080px;
            margin: 0 auto;
            border: 1px solid;
            padding: 10px;
        }

        .parent {
            height: 350px;
            border: 1px solid;
            display: flex;
            /* 수평배치 center,right,left,space-between,space-evenly space-around */
            justify-content: center;
            /* item간 여백지정없는 설정시 gap option 사용가능  */
            gap: 0px;
            /* 수직배치 start,end,center,flex-start,flex-end */
            align-items: center;
            /* 방향지정 : row , column row-reverse, column-reverse*/
            flex-direction: row;
            margin-bottom:50px;
        }

        .parent>.child {
            width: 120px;
            /* height : 40px; */
            border: 1px solid;
        }
        
        .parent2{
            border: 1px solid;
            display:flex;
            flex-wrap:wrap;

            justify-content: center;
            align-items: center;
            gap:10px;
        }
        .parent2>.child2{
            width: 200px;
            height:200px;
            border : 1px solid;
            background-color: antiquewhite;
        }
    </style>
</head>

<body>

    <div class="wrapper">
        <div class="parent">
            <div class="child">1</div>
            <div class="child">2</div>
            <div class="child">3</div>
            <div class="child">4</div>
            <div class="child">5</div>
        </div>

        <div class="parent2">
            <div class="child2">1</div>
            <div class="child2">2</div>
            <div class="child2">3</div>
            <div class="child2">4</div>
            <div class="child2">5</div>
            <div class="child2">6</div>
            <div class="child2">7</div>
            <div class="child2">8</div>
            <div class="child2">9</div>
            <div class="child2">10</div>
            <div class="child2">11</div>
            <div class="child2">12</div>
            <div class="child2">13</div>
            <div class="child2">14</div>
            <div class="child2">15</div>
            <div class="child2">16</div>
            <div class="child2">17</div>
            <div class="child2">18</div>
            <div class="child2">19</div>
            <div class="child2">20</div>
        </div>


    </div>


</body>

</html>
```

justify-content:
수평 정렬


|정렬방식|결과|
|-|-|
|left|왼쪽 정렬|
|right|오른쪽 정렬|
|space-between|양 끝 고정+ 간격 균등|
|space-around|양끝 포함 간격 균등|
|space-evenly|모든 간격 균등|


align-items:
수직 정렬
|정렬방식|결과|
|-|-|
|start|위쪽 정렬|
|center|가운데 정렬|
|end|하단 정렬|

flex-direction:

|정렬 방식|결과|
|-|-|
|row|가로(기본값)|
|column|세로|
|row-reverse|가로 뒤집기|
|column-reverse|세로 뒤집기|

---

## FLEX 02

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <style>
        .wrapper {
            /* width : 1280px; */
            height: 900px;
            border: 1px solid;
            margin: 0 auto;
            padding: 10px;
        }

        .wrapper>.parent {
            width: 100%;
            height: 150px;
            border: 1px solid;

            display:flex;
            align-items: center;
            flex-wrap: wrap;
        }

        .wrapper>.parent>.child {
            border: 1px solid;
        }
        /* 
            flex-grow   : flex 아이템의 증가 비율 설정 0(기본값-증가하지 않음)
            flex-shrink : flex 아이템의 감소 비율 설정 (0 - 감소하지 않음 1:기본값 너비에따라 감소)
            flex-basis  : 기본크기 지정
        */
        .wrapper>.parent>.child:nth-child(1){
            flex-grow : 1;
            flex-shrink: 0;
            flex-basis:200px;
        }
        .wrapper>.parent>.child:nth-child(2){
            flex-grow : 1;
            flex-shrink: 0;
            flex-basis:200px;            
        }
        .wrapper>.parent>.child:nth-child(3){
            flex-grow : 1;
            flex-shrink: 0;
            flex-basis:200px;            
        }
        .wrapper>.parent>.child:nth-child(4){
            flex-grow : 1;
            flex-shrink: 0;
            flex-basis:200px;            
        }
        .wrapper>.parent>.child:nth-child(5){
            flex-grow : 1;
            flex-shrink: 0;
            flex-basis:200px;            
        }
    </style>
</head>

<body>


    <div class="wrapper">
        <div class="parent">
            <div class="child">1</div>
            <div class="child">2</div>
            <div class="child">3</div>
            <div class="child">4</div>
            <div class="child">5</div>
        </div>
    </div>
</body>

</html>
```



|flex|grow(확장비율)|shrink(축소비율)|basis(기본크기)|
|-|-|-|-|
|속성|남는 공간을 얼마나 차지할지 설정|부모 공간이 부족할 때 최대 축소 설정| 요소의 기본 크기 설정|
|속성|0 : 기본값 , 남은 공간 차지X|0 : 줄어들지 않음|flex-grow, flex-shrink의 기준점이 되는 크기|
|속성|1 : 남는 공간을 균등하게 나눔|1 : 기본값 , 공간 부족시 비율에 따라 축소됨||


