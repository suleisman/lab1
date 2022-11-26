```
#include <stdio.h>

int main()
{
    
    char c;
    int n=0;
    int v[n];

int i=0;

int  sum=0;
int a=0;
int b=0;
   
for(char c=getchar();c!='\n';c=getchar())
{
    if(c!=' ')
    {
        int p_1=c-48;

       
        sum=sum+p_1;
    
     
    }
    else
    {if(c==' '&&(i%2==0))
    {
        
        a=sum;
       
        sum=0;
        i++;
    }else{ if(c==' '&&(i%2!=0))
    {
        
        b=sum;
       
        sum=0;
        i++;
    }}}
   
}

if(i%2==1)
{
    printf("%d", a);
}
else
{
    printf("%d", b);
}
    return 0;
}

```
```
#include <stdio.h>



int main() {
    FILE * file;


    int i=0;
    int  sum=0;
    int a=0;
    int b=0;
    file=fopen("test.txt","r");
    char c;
    for(  c=getc(file); c!=EOF;c=getc(file)) {

        if(c!=' ') {
            int p_1=c-48;
            sum=sum+p_1;
        }
        else { 
            if(c==' '&&(i%2==0)) {
                a=sum;
                sum=0;
                i++;
            }
            else {
                if(c==' '&&(i%2!=0)) {
        
                    b=sum;
        	    sum=0;
                    i++;
                }
            }
        }
   
    }

    if(i%2==1) {
        printf("%d", a);
    }
    else {
        printf("%d", b); 
    }

    fclose(file);

    return 0;
}
```

```

#include <stdio.h>
#include <stdlib.h>

enum State {
    INSIDE,
    OUTSIDE
};

int f();

int main(void) {
    printf("%d\n", f());
    return 0;
}

int f() {
    enum State state = INSIDE;
    char c;
   
    int i = 0;

    int sum = 0;
    int a = 0;
    int b = 0;
   
    for(char c = getchar();c!=EOF;c = getchar()) {
        if(c!=' ') {
            int p_1 = c - 48;
            sum = sum + p_1;
        }
        else { 
            switch (state) {
                case INSIDE:
                     if(c == ' ') {
                        a = sum;
                        sum = 0;
                        state = OUTSIDE;
                        break;
                     }
                case OUTSIDE:
                    if(c == ' ') {
        
                        b = sum;
                        sum = 0;
                        state = INSIDE;
                        break;
                    }
            }
        }
    }

    if(state==OUTSIDE) {
        return a;
    }
    else {
        return  b;
    }
}
```

```
#include <stdio.h>
#include <stdlib.h>

struct A{
 int x;
 int y;
};


enum State {
    INSIDE,
    OUTSIDE
};


struct A f() {
    
    struct A d;
    enum State state = INSIDE;
   
   
    int i = 0;

    int sum = 0;
    int a = 0;
    int b = 0;
    int now_a=0;
    int now_b=0;
    int now=0;
   
    for(char c = getchar();c!='\n';c = getchar()) {
        if(c!=' ') {
            int p_1 = c - 48;
            sum = sum + p_1;
            now=now*10+(c-48);
        }
        else { 
            switch (state) {
                case INSIDE:
                     if(c == ' ') {
                        now_a=now; 
                        a = sum;
                        sum = 0;
                        now=0;
                        state = OUTSIDE;
                        break;
                     }
                case OUTSIDE:
                    if(c == ' ') {
                        now_b=now;
                        b = sum;
                        sum = 0;
                        now=0;
                        state = INSIDE;
                        break;
                    }
            }
        }
    }

    if(state==OUTSIDE) {
        d.x = now_a;
        d.y=a;    
        
            
    } 
    else {
        d.x=now_b;
        d.y=b;
    
    }
       return d;
    }
    






int main(int argc, char **argv)
{
    struct A ans=f();
    printf("%d %d", ans.x, ans.y);
    return 0;
}

```

