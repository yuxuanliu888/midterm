// var mysound
// function preload(){
// soundFormats("mp3")
//   mysound =loadSound("123.mp3")
// }

function setup() {
  createCanvas(400, 400);
}
var x1=400
var y1=0
var x2=0
var y2=400
    var x3=400
    var y3=400
var cc=35

var x4=200
var y4=190
var p= 0
var k=0
var Vqiu=0.3

var bian=1
function draw() {
  background(220,20);
  fill(135,20,cc)
  noStroke()
  triangle(x1,y1,x2,y2,x3,y3)
  triangle(x2,y2,x2,400,x3,y3)
  ellipse(x4,y4,10)

  y4=k*x4+400-y1-5
  k=(y2-y1)/(x2-x1)
  
    y1=y1-bian,
    y2=y2+bian
  
  if(y1<random(-30,10)||y1>random(400,600)){bian=random(-3,3)}

  //Vqiu=Vqiu*1 
 
//if(y4>x4)
  {}
  if (k<0){x4=x4*0.999}
   if (k>0){x4=x4*1.001}
  
  
  if(x4<=0&&y1>y2){win}

  
  if(x4<=0&&y1<y2){lose}
    
  if(x4>=width&&y1>y2){lose}
  
  if(x4>=width&&y1<y2){win}

  
  
  if (keyIsDown(LEFT_ARROW)){
    x4=x4-Vqiu

     } 
   if (keyIsDown(RIGHT_ARROW)){
     x4=x4+Vqiu

     } 
}
