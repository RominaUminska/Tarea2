# Tarea2

matriz rect;
matriz rect1;


void setup (){ //con el que se inicializa todo
  size (400,400);
  rect = new matriz (50,50,40,100,50,50);
  rect1 = new matriz (200,50,40,100,200,50);
}


void draw (){
 
background (255); 
rect.display(); 
rect.crecer();
rect1.display();
rect1.crecer();

}


class matriz {
  //describir los atributos
  int x;
  int y;
  int t;
  int i;
  int j;
  int u;
  
  
 //describir el metodo de construccion de clase
 
 matriz (int x_, int y_,int t_,int i_, int j_,int u_){
   x= x_;
   y= y_;
   t= t_;
   i= i_;
   j= j_;
   u= u_;
    
 }
   
   void crecer (){

if ((mouseX >= x & mouseX <= 150) & (mouseY >= 50 & mouseY <= 150)) {
  t= 20;
}
else {
t= 10;
}
if ((mouseX >= x & mouseX <= 300) & (mouseY >= 50 & mouseY <= 150)) {
t= 20;
}
else {
t=10;
}
}

void display(){
  noStroke();
for (int i = 0; i<u; i+=t){
for (int j = 0; j<u; j+=t){
fill (random(255));
rect (x+i,y+j,t,t);
}
}
}
}
