#include<stdio.h>
int main()
{
	int i,j,t,a[10],k,n;
	n=0;
	printf("This exam full score is 100,and the score below 60 is failing.\n");
	printf("Please input the Chinese scores of ten students：");
	for(j=0;j<10;j++)
		scanf("%d",&a[j]);
	printf("\n");
	for(i=0;i<9;i++)
	{
		k=i;
		for(j=i+1;j<10;j++)
			if(a[k]>a[j])
				k=j;
		if(i!=k)
		{t=a[k];a[k]=a[i];a[i]=t;}
	}
	printf("sort in descending order：\n");
	for(j=0;j<10;j++)
		printf("%4d",a[j]);
	for(j=0;j<10;j++)
	{if(a[j]<60)
	n++;}
	printf("\n");
	printf("The number of failed students：%d",n);
	return 0;
}
