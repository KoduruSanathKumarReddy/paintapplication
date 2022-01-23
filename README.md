# Web Page for Paint Application

## AIM:

To design a static website for Paint Application using HTML5 canvas.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML,CSS and canvas.

### Step 3:

Write javascript to capture move events.

### Step 4:

Perform the drawing operation based on the user input.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>multipleCanvas</title>
    <style>
        .maincontainer{
            text-align: center;
            display: inline;
           
        }
        .shapestoolbar{
            border: black;
            border-style:solid;
            width :100px;
            height:auto;
            margin-top:-600px;
            margin-left:200px;
        }
        .colorstoolbar{
            border:black;
            border-style: solid;
            width: 100px;
            height: auto;
            margin-left: 1150px;
            margin-top: -165px;
        }
        .colorstoolbar1{
            border:black;
            border-style: solid;
            width: 100px;
            height: auto;
            margin-left: 1150px;
            margin-top: 0px;
        }
        .values{
            border:black;
            border-style: solid;
            width: 200px;
            height: auto;
            margin-top: -400px;
            margin-left: 100px;

        }
        .paintarea{
            margin-left: 100px;
        }
        .shapebutton{
            width:70px;
            height:20px;
        }
        .buttonpad{
            margin-top: 5px;
            margin-bottom: 5px;
        }
        .text{
            margin-top: 5px;
            margin-bottom: 10px;
        }
        h1{
            margin-top: auto;
            margin-bottom: auto;
            text-decoration: underline;
        }
        body{
            background-image: url("https://wallpaperaccess.com/full/284607.jpg");
            background-repeat: no-repeat;
            background-size: cover;
        }
        .canvas{
            background-color: white;
        }
        .footer{
            color: black;
            padding-left: 550px;
            padding-top: 160px;
            font-size: 20px;
        }

    </style>

<script type="text/javascript">
var shape;
var color;
var color2;
var radius, side, width, height,linewidth;

function myClickEvent(e){
        var ctx = c.getContext("2d");
        ctx.beginPath();
        radius =document.getElementById("radius");
        side = document.getElementById("SquareSide");
        width = document.getElementById("width");
        height = document.getElementById("height");
        linewidth = document.getElementById("lwidth");
        radiusValue = parseInt(radius.value);
        sideValue = parseInt(side.value);
        widthValue = parseInt(width.value);
        heightValue = parseInt(height.value);
        lwidhtValue = parseInt(linewidth.value);
        if(color2==1){
            ctx.fillStyle="red";
        }else if(color2==2){
            ctx.fillStyle="yellow";
        }else if(color2==3){
            ctx.fillStyle="blue";
        }else if(color2==4){
            ctx.fillStyle="orange";
        }else if(color2==5){
            ctx.fillStyle="green";
        }else if(color2==6){
            ctx.fillStyle="violet";
        }else if(color2==7){
            ctx.fillStyle="black";
        }else if(color2==8){
            ctx.fillStyle="white";
        }else if(color2==9){
            ctx.fillStyle="pink";
        }else{
            ctx.fillStyle="rgba(0, 0, 200, 0)";
        }
        if(color==1){
            ctx.strokeStyle='red';
        }else if(color==2){
            ctx.strokeStyle='yellow';

        }else if(color==3){
            ctx.strokeStyle='blue';
        }else if(color==4){
            ctx.strokeStyle='orange';
        }else if(color==5){
            ctx.strokeStyle='green';
        }else if(color==6){
            ctx.strokeStyle='violet';
        }else if(color==7){
            ctx.strokeStyle='black';
        }else if(color==8){
            ctx.strokeStyle='white';
        }else if(color==9){
            ctx.strokeStyle='pink';
        }
        if(shape == 0){
            ctx.lineWidth=lwidhtValue;
            ctx.arc(e.offsetX,e.offsetY, radiusValue, 0, 2 * Math.PI);
            ctx.fill();
            ctx.stroke();
            
        }else if(shape == 1){
            ctx.lineWidth=lwidhtValue;
            ctx.moveTo(e.offsetX,e.offsetY);
            ctx.lineTo(100,200);
            ctx.fill();
            ctx.stroke();
        }else if(shape==2){
            ctx.lineWidth=lwidhtValue;
            ctx.rect(e.offsetX,e.offsetY, widthValue,heightValue);
            ctx.fill();
            ctx.stroke();


        }else if(shape==3){
            ctx.lineWidth=lwidhtValue;
            ctx.rect(e.offsetX, e.offsetY, sideValue,sideValue);
            ctx.fill();
            ctx.stroke();

        }else if(shape==4){
            ctx.lineWidth=lwidhtValue;
            ctx.moveTo(100,100);
            ctx.lineTo(100, 300);
            ctx.lineTo(300, 300);
            ctx.closePath();
            ctx.fill();
            ctx.stroke();
            
        }
    }
        function circleClicked(){
            shape=0;
        }
        function lineClicked(){
            shape=1;
        }
        function rectangleClicked(){
            shape=2;
        }
        function squareClicked(){
            shape=3;
        }
        function trinagleClicked(){
            shape=4;
        }
        function redClicked(){
            color=1;
        }
        function yellowClicked(){
            color=2;
        }
        function blueClicked(){
            color=3;
        }
        function orangeClicked(){
            color=4;
        }
        function greenClicked(){
            color=5;
        }
        function violetClicked(){
            color=6;
        }
        function blackClicked(){
            color=7;
        }
        function whiteClicked(){
            color=8;
        }
        function pinkClicked(){
            color=9;
        }
        function redClicked1(){
            color2=1
        }
        function yellowClicked1(){
            color2=2
        }
        function blueClicked1(){
            color2=3
        }
        function orangeClicked1(){
            color2=4
        }
        function greenClicked1(){
            color2=5
        }
        function violetClicked1(){
            color2=6
        }
        function blackClicked1(){
            color2=7
        }
        function whiteClicked1(){
            color2=8
        }
        function pinkClicked1(){
            color2=9
        }
        


</script>
</head>
<body>
    <div class="maincontainer">
        <h1>Canvas Drawing Application</h1>
        <div class="paintarea"><canvas class="canvas" id="myCanvas" width="800" height="600" style="border:1px solid #000000"></canvas></div>
        <div class="shapestoolbar">
            <h4 class="text"><u>Shapes</u></h4>
            <div class="buttonpad"><input class="shapebutton" type="button" id="circle" value="Circle"><br></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="line" value="Line"><br></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="rectangle" value="Rectangle"><br></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="square" value="Square"><br></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="triangle" value="Triangle"><br></div>

        </div>
        <div class="colorstoolbar">
            <h4 class="text"><u>Colors-1</u></h4>
            <div class="buttonpad"><input class="shapebutton" type="button" id="red" value="" style="background-color: red;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="yellow" value="" style="background-color: yellow;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="blue" value="" style="background-color: blue;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="orange" value="" style="background-color: orange;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="green" value="" style="background-color: green;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="violet" value="" style="background-color: violet;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="black" value="" style="background-color:black;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="white" value="" style="background-color: white;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="pink" value="" style="background-color: pink;"></div>
        </div>
        <div class="colorstoolbar1">
            <h4 class="text"><u>Colors-2</u></h4>
            <div class="buttonpad"><input class="shapebutton" type="button" id="red1" value="" style="background-color: red;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="yellow1" value="" style="background-color: yellow;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="blue1" value="" style="background-color: blue;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="orange1" value="" style="background-color: orange;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="green1" value="" style="background-color: green;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="violet1" value="" style="background-color: violet;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="black1" value="" style="background-color:black;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="white1" value="" style="background-color: white;"></div>
            <div class="buttonpad"><input class="shapebutton" type="button" id="pink1" value="" style="background-color: pink;"></div>
            
            
        </div>
        <div class="values">
            <h4 class="text"><u>Scale</u></h4>
            <label>Line Width:</label>
            <input type="number" id="lwidth">
            <label>Circle Radius:</label>
            <input type="number" id="radius"><br>
            <label>Square Side:</label>
            <input type="numbe" id="SquareSide"><br>
            <label>Rectange width,height</label>
            <input type="number" id="width"><input type="number" id="height"><br>
            

        </div>
      
    </div>
    <div class="footer">
        <h4>Developed By: Koduru Sanath Kumar Reddy</h4>
    </div>
        <script type ="text/javascript">
            var c = document.getElementById("myCanvas");
            c.addEventListener("click", myClickEvent);
            document.getElementById("circle").addEventListener("click", circleClicked);
            document.getElementById("line").addEventListener("click",  lineClicked);
            document.getElementById("rectangle").addEventListener("click", rectangleClicked);
            document.getElementById("square").addEventListener("click", squareClicked);
            document.getElementById("triangle").addEventListener("click", trinagleClicked);
            document.getElementById("red").addEventListener("click",redClicked);
            document.getElementById("yellow").addEventListener("click",yellowClicked);
            document.getElementById("blue").addEventListener("click",blueClicked);
            document.getElementById("orange").addEventListener("click",orangeClicked);
            document.getElementById("green").addEventListener("click",greenClicked);
            document.getElementById("violet").addEventListener("click",violetClicked);
            document.getElementById("black").addEventListener("click",blackClicked);
            document.getElementById("white").addEventListener("click",whiteClicked);
            document.getElementById("pink").addEventListener("click",pinkClicked);
            document.getElementById("red1").addEventListener("click",redClicked1);
            document.getElementById("yellow1").addEventListener("click",yellowClicked1);
            document.getElementById("blue1").addEventListener("click",blueClicked1);
            document.getElementById("orange1").addEventListener("click",orangeClicked1);
            document.getElementById("green1").addEventListener("click",greenClicked1);
            document.getElementById("violet1").addEventListener("click",violetClicked1);
            document.getElementById("black1").addEventListener("click",blackClicked1);
            document.getElementById("white1").addEventListener("click",whiteClicked1);
            document.getElementById("pink1").addEventListener("click",pinkClicked1);

        </script>
</body>
</html>
~~~

## OUTPUT:

![](canvas1.png)
![](canvas2.png)
![](canvas3.png)

## Result:

Thus a website is designed and validated for paint application using HTML5 canvas.
