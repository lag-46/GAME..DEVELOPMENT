# EX 7 : THREE DIMENSIONAL TRANSFORMATIONS

## AIM :
 
 To implement the various transformations on three dimensional odjects using a c coding.

## EQUIPMENT REQUIRED:

●	Hardware: Personal Computer (PC)

●	Software: C Compiler

## ALGORITHM :


   Step 1 : Start.

   Step 2 : Draw an image with default parameters.

   Step 3 : Get the choice from user.

   Step 4 : Get the parameters for transformation.

   Step 5 : Perform the transformation.

   Step 6 : Display the output.

   Step 7 : Stop.

## Program :

```
#include<stdio.h> 
#include<conio.h> 
#include<graphics.h> 
#include<math.h> 
int maxx,maxy,midx,midy; 
void axis() 
{ 
getch(); 
cleardevice(); 
line(midx,0,midx,maxy); 
line(0,midy,maxx,midy); 
} 
void main() 
{ 
int gd,gm,x,y,z,o,x1,x2,y1,y2; 
detectgraph(&gd,&gm); 
initgraph(&gd,&gm,"C://TURBOC3//BGI"); 
setfillstyle(0,getmaxcolor()); 
maxx=getmaxx(); 
maxy=getmaxy(); 
midx=maxx/2; 
midy=maxy/2; 
axis(); 
bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
printf("Enter Translation Factor"); 
scanf("%d%d%d",&x,&y,&z); 
axis(); 
printf("after translation"); 
bar3d(midx+(x+50),midy-(y+100),midx+x+60,midy-(y+90),5,1); 
axis(); 
bar3d(midx+50,midy+100,midx+60,midy-90,5,1); 
printf("Enter Scaling Factor"); 
scanf("%d%d%d",&x,&y,&z); 
axis(); 
printf("After Scaling"); 
bar3d(midx+(x*50),midy-(y*100),midx+(x*60),midy-(y*90),5*z,1); 
axis(); 
bar3d(midx+50,midy-100,midx+60,midy-90,5,1); 
printf("Enter Rotating Angle"); 
scanf("%d",&o); 
x1=50*cos(o*3.14/180)-100*sin(o*3.14/180); 
y1=50*cos(o*3.14/180)+100*sin(o*3.14/180); 
x2=60*sin(o*3.14/180)-90*cos(o*3.14/180); 
y2=60*sin(o*3.14/180)+90*cos(o*3.14/180); 
axis(); 
printf("After Rotation about Z Axis"); 
bar3d(midx+x1,midy-y1,midx+x2,midy-y2,5,1); 
axis(); 
printf("After Rotation about X Axis"); 
bar3d(midx+50,midy-x1,midx+60,midy-x2,5,1); 
axis(); 
printf("After Rotation about Y Axis"); 
bar3d(midx+x1,midy-100,midx+x2,midy-90,5,1); 
getch(); 
closegraph(); 
}
```
## Output :

<img width="642" height="507" alt="Screenshot 2025-10-24 160033" src="https://github.com/user-attachments/assets/1f2931c0-0ddf-4d03-83e1-f6dc6b34fe92" />

<img width="637" height="510" alt="Screenshot 2025-10-24 160042" src="https://github.com/user-attachments/assets/d0516efe-ae87-4a3a-86a5-5816841dafd7" />

<img width="639" height="503" alt="Screenshot 2025-10-24 160103" src="https://github.com/user-attachments/assets/cbe68e01-e900-4fcd-bb05-45999d40f735" />


<img width="643" height="512" alt="Screenshot 2025-10-24 160113" src="https://github.com/user-attachments/assets/6994b7b6-f140-4255-962e-ed608cda0fe4" />


<img width="640" height="513" alt="Screenshot 2025-10-24 160124" src="https://github.com/user-attachments/assets/fe60c307-6796-4332-b5bd-f8a0d59edfd0" />


<img width="638" height="510" alt="Screenshot 2025-10-24 160131" src="https://github.com/user-attachments/assets/961eb4cf-5b01-4c87-9d46-c06124a49662" />


<img width="638" height="507" alt="Screenshot 2025-10-24 160139" src="https://github.com/user-attachments/assets/4421a0b8-9457-479d-828a-56d666c5fb97" />


<img width="638" height="508" alt="Screenshot 2025-10-24 160150" src="https://github.com/user-attachments/assets/e56e4117-6edb-47fa-91f3-067144b26fca" />

## Result :
 Thus the program was executed and the output was obtained successfully.
