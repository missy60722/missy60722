#include<stdio.h>   
#include<stdlib.h>  
void DecToN(int n, int b)
{
	int i=0, j, r;
	int a[100]; 
	printf("n=", n);

	while(n>=b) 
	{
		r=n%b;
		n=n/b;
		a[i]=r;
		i++;
		//printf("%d ", r ) ;	
	}
	a[i]=n;
		//printf("%d ",n);
	for(j=i;j>=0;j--)
	{
		printf("%d" ,a[j]);
	}

 } 
 
int main()         
//第一頁面
{
	char ans;
	printf("\n");
	printf("\n");
	printf("                                    歡迎使用進位換算計算機\n");
	printf("\n");
	printf("\n");
	printf("介紹:在這裡，你可以輸入二進位或八進位或十進位的數字，我們會幫你轉換成你輸入之外的兩種進位方式\n");
	printf("\n");

	printf("\n");
	printf("使用限制:若輸入二進位，則數字只可輸入0到1\n");        
	printf("         若輸入八進位，則數字只可輸入0到7\n");	
	printf("         若輸入十進位，則數字只可輸入0到9\n");	
	printf("\n");
	printf("\n");
	
	do
	{
		printf("\n");
		printf("使用規則:若選擇十進位，請輸入A\n");
		printf("使用規則:若選擇八進位，請輸入B\n"); 
		printf("使用規則:若選擇二進位，請輸入C\n");
		char type;
		scanf(" %c", &type);
	
		int num=0, r, n;
		printf("輸入一個數:");
		scanf("%d", &num);
		if (type=='A')
		{
			//	十進制轉二進制 
			printf("\n");
			printf("二進制");
			DecToN(num, 2);
			printf("\n");
			//	十進制轉八進制 
			printf("八進制");
			DecToN(num, 8);
		
		
			printf("\n");
			printf("還要繼續嗎(y/n?)");
			printf("\n");
			scanf(" %c",&ans);
		}
	}while(ans=='y'||ans=='Y');

	printf("謝謝使用");
	printf("\n");
	printf("我們是一年和班");

return 0;
    
}	
