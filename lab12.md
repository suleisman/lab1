```
#include <stdio.h>
#include <stdlib.h>

enum State {
    INSIDE,
    OUTSIDE
};

int f_1();


int main(void) {
    printf("%d ",f_1());

    return 0;
}

int f_1() {
    enum State state = INSIDE;
    char c;
   
    int i = 0;

    int sum = 0;
    int now=0;
    int now_1=0;
    int now_2=0;
   
   for(char c=getchar() ;c!='\n'; c=getchar()) {
       switch (state) {
           case INSIDE:
                now_1=c-48;
                sum=sum*10+now_1;
                now=now + now_1;
                state=OUTSIDE;
                break;
            case OUTSIDE:
                now_2=c-48;
                sum=sum*10+now_1;
                now=now + now_1;
                if(now<10) {
                    sum=sum*10+now;
                    now=0;
                } else {
                    now=0;
                }
                state= INSIDE;
                break;
                
                
                
       }
       
       
   }
   return sum;
    
}

```
