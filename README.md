#include<stdio.h>
#include<math.h>

int checkprime(int n){
	for(int i=2;i <= sqrt(n);i++){
		if(n%i==0) return 0;
		return 1;
	}
}

int main(){
	int n;
	printf("\nPrint prime number from 2 to n program\n");
	printf("Enter n>=2 : ");
	do{
		fflush(stdin); scanf("%d",&n);
		if(n<2)
			printf("\nInput wrong!\nEnter again: ");
	}while(n<2);
	printf("\nAll prime number from 2 to %d :",n);
	for(int i=2;i<=n;i++){
		if(checkprime(i)==1) printf("%d,",i);
	}
	return 0;
}
