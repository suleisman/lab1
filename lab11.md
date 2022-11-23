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
