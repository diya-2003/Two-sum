#include <stdio.h>
int re[2];
int *check(int*s,int l,int t)
{
	for(int i=0;i<l;i++)
	{
		for(int j=i+1;j<l;j++)
		{
			if(s[i]+s[j]==t)
			{
				re[0]=i;
				re[1]=j;
				return re;
			}
		}
	}
}
int main()
{
	int n,s[n],t;
	printf("\nEnter the range:");
	scanf("%d",&n);
	printf("\nEnter the array:");
    for(int i=0;i<n;i++){
    scanf("%d",&s[i]);}
    printf("\nEnter the target:");
    scanf("%d",&t);
	int *in=check(s,n,t);
	if(in != NULL)
			printf("%d %d\n",in[0],in[1]);
	else
		printf("noooo");
	return 0;
}
