//CLIMBING A HILL

//Press "SHIFT" to begin the music
//Press "LEFT" and "RIGHT" Keys to control your small ball
//If you climb to the higher part of the mountain, you "WIN"
//If you slide to the lower part of the mountain, you "LOSE"
//The gmae will be harder after you won a game
var mysound
 function preload(){
 soundFormats("mp3")
  mysound =loadSound("321.mp3")
 }

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

var kbian1=0.999
var kbian2=1.001
var bian=1
var biana=-3
var bianb=3
var level = [1,2,3]
var a=1
var flash=30

var back=220
var t=0.5
function draw() {
  
  
    
  background(back,20);
  
  
  fill(135,20,cc)
  noStroke()

  triangle(x1,y1,x2,y2,x3,y3)
  triangle(x2,y2,x2,400,x3,y3)
  ellipse(x4,y4,10)


  
  y4=k*x4+400-y1-5
  k=(y2-y1)/(x2-x1)
  
    y1=y1-bian,
    y2=y2+bian
  
  if(y1<random(-30,10)||y1>random(400,600)){bian=random(biana,bianb)}
  

  //daojuy=daojuy+1
  
  //if(daojuy=daojux*k+400){daojux=daojux+1}
  
  //Vqiu=Vqiu*1 
 
//if(y4>x4)

  if (k<0){x4=x4*kbian1}
   if (k>0){x4=x4*kbian2}
 //  textSize(30)
 // text('Level ',150,40)
  
  if(x4<=0&&y1>y2){textSize(60);rect(0,0,400,400);fill(300, 300, 300);text('Win',150,210);bian=0;textSize(20);text('Click Enter To the Next Leval',70,250)
                       
       if(keyIsDown(ENTER)){x4=200,k=k+0.1,bian=random(-3,3),kbian1=kbian1*0.998,kbian2=kbian2*1.002,biana=biana-3,bianb=bianb+3,back=random(0,20)}  
                   
                  }//win

  
  
  if(x4<=0&&y1<y2){textSize(60);rect(0,0,400,400);fill(300, 300, 300);text('Lose',150,210);bian=0;textSize(20);text('Click Enter To the Next Leval',70,250)
        //Lose
                   
       if(keyIsDown(ENTER)){x4=200,k=k+0.001,bian=random(-3,3),biana=biana*0.99,bianb=bianb*0.99,back=random(200,300)} }
  
  
  if(x4>=width&&y1>y2){textSize(60);rect(0,0,400,400);fill(300, 300, 300);text('Lose',150,210);bian=0;textSize(20);text('Click Enter To the Next Leval',70,250)
                   
       if(keyIsDown(ENTER)){x4=200,k=k+0.001,bian=random(-3,3),biana=biana*0.999,bianb=bianb*0.999,back=random(150,300)}   }
  //Lose111
  
  
  if(x4>=width&&y1<y2){textSize(60);rect(0,0,400,400);fill(300, 300, 300);text('Win',150,210);bian=0;textSize(20);text('Click Enter To the Next Leval',70,250)
                   
       if(keyIsDown(ENTER)){x4=200,k=k+0.1,bian=random(-3,3),kbian1=kbian1*0.998,kbian2=kbian2*0.999,biana=biana-3,bianb=bianb+3,back=random(0,30)} }
//Win
  
  
  if (keyIsDown(LEFT_ARROW)){
    x4=x4-Vqiu 

     } 
   if (keyIsDown(RIGHT_ARROW)){
     x4=x4+Vqiu

     } 
 // function keyPressed(SHIFT) 
 if (keyIsDown(SHIFT)){mysound.play()}
  
  
  
}
