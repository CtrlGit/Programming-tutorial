##答え
```c
#include <stdio.h>

void main(void){
    int a,b;

    scanf("%d %d",&a,&b);

    if(a>b){
      printf("%d\n",a);
    }
    else if(a<b){
      printf("%d\n",b);
    }
    else{
      printf("同じです\n");
    }

}
```
