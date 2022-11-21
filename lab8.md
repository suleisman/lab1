```
#include <stdio.h>
#include <stdlib.h>
#include <math.h>



int main()
{
 

 


    double x0,y0,x,y,a,b,c,r;
  
    scanf("%lf %lf",&x0,&y0);
 
    scanf("%lf",&r); 

    scanf("%lf %lf  %lf",&a,&b,&c);





    double k=-(a/b);
    double l=-(c/b);

 
    double d1 = k*k + 1;
    double d2 = 2 * k * (l - y0) - 2 * x0;
    double d3 = x0*x0 - r*r + (l - y0)*(l - y0);
    double D = d2*d2 - 4 * d1 * d3;
    if (D >= 0) {
        double x1 = (-d2 - sqrt(D)) / (2. * d1);
        double y1 = k * x1 + l;
        double x2 = (-d2 + sqrt(D)) / (2. * d1);
        double y2 = k * x2 + l;
        printf("%lf %lf\n %lf %lf\n",x1,y1,x2,y2); 
    }



      
  
 
  
    return 0;
}
```
