##答え
問題1
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

問題2
```c
#include <stdio.h>

void main(void){
    int a;

    scanf("%d",&a);

    if(a%2 == 0){
      printf("偶数です\n");
    }
    else{
      printf("奇数です\n");
    }

}
