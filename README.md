# projetolop8
//etapa 8
var xin2=[]
var yin2=[]
var qtdObjetosn2=10
var vidas=5
var pontos=0
var nivel=1
var vxi=[]
var vyi=[]
var qtdObjetos=10
var raioO=15
var raioP=10
var x=10
var y=200
var xd
var yd
var bpontos=9
var estadoDisparo = false;
var raioD=3
function setup() {
  createCanvas(400, 400);
  for(i=0;i<=qtdObjetos;i++){
  vxi[i]=random(50,400)
  vyi[i]=random(50,400) 
}
   for(i=1;i<qtdObjetosn2;i++){
     xin2[i]=random(50,400)
  yin2[i]=random(50,400)}
}
function draw() {
  background(100);
   textSize(19);
  text('vidas: '+vidas,10,30);
  text('nivel: '+nivel,200,30)
  text('pontos:  '+pontos,300,30)
  for(i=1;i<=qtdObjetos;i++){
  ellipse(vxi[i],vyi[i],2*raioO,2*raioO)
  }
  ellipse(x,y,2*raioP,2*raioP)
   if ( keyIsDown(RIGHT_ARROW) )
  {
    x=x+4
  }
   if ( keyIsDown(LEFT_ARROW) )
  {
    x=x-4
  }
  if ( keyIsDown(UP_ARROW) )
  {
    y=y-4
  }
    if ( keyIsDown(DOWN_ARROW) )
  {
    y=y+4
  }
    ellipse(xd,yd,1*raioD,1*raioD)
  if ( keyIsDown(CONTROL) && ! estadoDisparo)
  {
    xd=x
    yd=y
    estadoDisparo = true;
  }

if( estadoDisparo ) {
  ellipse(xd,yd,1*raioD,1*raioD)
  xd=xd+10;
}
  if(xd > 400)
  {
    estadoDisparo=false
  }
  if(dist(x,y,vxi[1],vyi[1])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
  if(dist(x,y,vxi[2],vyi[2])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
   if(dist(x,y,vxi[3],vyi[3])< raioO + raioP)
  {
    x=10
    y=200
    vidas=vidas-1
  }
    if(dist(x,y,vxi[4],vyi[4])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
     if(dist(x,y,vxi[5],vyi[5])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
       if(dist(x,y,vxi[6],vyi[6])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
       if(dist(x,y,vxi[7],vyi[7])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
       if(dist(x,y,vxi[8],vyi[8])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
      if(dist(x,y,vxi[9],vyi[9])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
     if(dist(x,y,vxi[10],vyi[10])< raioO + raioP)
  {
    x=10
    y=200
      vidas=vidas-1
  }
    if(dist(xd,yd,vxi[1],vyi[1])< raioO + raioD)
  {
    vxi[1]=0
       vyi[1]=0
      pontos=pontos+1
  }
  if(dist(xd,yd,vxi[2],vyi[2])< raioO + raioD)
  {
   vxi[2]=0
       vyi[2]=0
      pontos=pontos+1
  }
   if(dist(xd,yd,vxi[3],vyi[3])< raioO + raioD)
  {
   vxi[3]=0
       vyi[3]=0
      pontos=pontos+1
  }
    if(dist(xd,yd,vxi[4],vyi[4])< raioO + raioD)
  {
    vxi[4]=0
       vyi[4]=0
      pontos=pontos+1
  }
     if(dist(xd,yd,vxi[5],vyi[5])< raioO + raioD)
  {
   vxi[5]=0
       vyi[5]=0
      pontos=pontos+1
  }
       if(dist(xd,yd,vxi[6],vyi[6])< raioO + raioD)
  {
   vxi[6]=0
       vyi[6]=0
      pontos=pontos+1
  }
       if(dist(xd,yd,vxi[7],vyi[7])< raioO + raioD)
  {
   vxi[7]=0
       vyi[7]=0
      pontos=pontos+1
  }
       if(dist(xd,yd,vxi[8],vyi[8])< raioO + raioD)
  {
    vxi[8]=0
       vyi[8]=0
      pontos=pontos+1
  }
      if(dist(xd,yd,vxi[9],vyi[9])< raioO + raioD)
  {
  vxi[9]=0
       vyi[9]=0
      pontos=pontos+1
  }
     if(dist(xd,yd,vxi[10],vyi[10])< raioO + raioD)
  {
       vxi[10]=0
       vyi[10]=0
      pontos=pontos+1
  }
 if(pontos>bpontos){
    nivel=2;
    bpontos==bpontos+10 ;
   raioO=0
   
   for(i=1;i<qtdObjetosn2;i++){
     ellipse(xin2[i],yin2[i],20,20)}
   yin2[1]=yin2[1]-1
    yin2[2]=yin2[2]-2
     yin2[3]=yin2[3]-3
      yin2[4]=yin2[4]-2
       yin2[5]=yin2[5]-1
        yin2[6]=yin2[6]-2
         yin2[7]=yin2[7]-4
          yin2[8]=yin2[8]-2
           yin2[9]=yin2[9]-1
            yin2[10]=yin2[10]-1
   if(yin2[1]<50){
     yin2[1]=400}
     if(yin2[1]<50){
     yin2[1]=400}
     if(yin2[2]<50){
     yin2[2]=400}
     if(yin2[3]<50){
     yin2[3]=400}
     if(yin2[4]<50){
     yin2[4]=400}
     if(yin2[5]<50){
     yin2[5]=400}
     if(yin2[6]<50){
     yin2[6]=400}
     if(yin2[7]<50){
     yin2[7]=400}
     if(yin2[8]<50){
     yin2[8]=400}
     if(yin2[9]<50){
     yin2[9]=400}
     if(yin2[10]<50){
     yin2[10]=400}
 }
}
