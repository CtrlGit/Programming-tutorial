```c
#include <stdio.h>
void main(void){
	int a[5];
	int i = 0;
	int max = 0;

	scanf("%d %d %d %d %d", &a[0], &a[1], &a[2], &a[3], &a[4]);

	max = a[0];

	for (i = 1; i <= 4; i++){
		if (max < a[i]){
			max = a[i];
		}
	}

	printf("入力された中で一番大きい整数は%dです\n", max);


}
```
