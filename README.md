# 6666
v01111
#include<stdio.h>
int main(void)
{
	char a[]="3+4";
	int b,c,d;
	b=a[0]-'0';
	c=a[2]-'0';
	d=b+c;
	printf("%d",d);
	return 0;
 }
 #include<stdio.h>
#include<string.h>
int main(void)
{
	char a[]="1+2+2+1+2+5+4-1-3+4-8";
	int sum=0;
	for(int i=1;i<strlen(a);i+=2)
		if(a[i]=='+')
			sum=sum+(a[i+1]-'0');
		else if(a[i]=='-')
			sum=sum-(a[i+1]-'0');
	 int c;
	 c=a[0]-'0';
	 int x;
	 x=c+sum;
	 printf("%d",x);
	return 0;
}
#include<stdio.h>
#include<string.h>
int main(void)
{
	char a[]="1+2+2+1+2+5+4-1-3+4-8";
	int sum=0;
	for(int i=1;i<strlen(a);i+=2)
		if(a[i]=='+')
			sum=sum+(a[i+1]-'0');
		else if(a[i]=='-')
			sum=sum-(a[i+1]-'0');
	 int c;
	 c=a[0]-'0';
	 int x;
	 x=c+sum;
	 printf("%d",x);
	return 0;
}
#include<stdio.h>
#include<string.h>
int main()
{
	char a[]="2*3*4-6+7-2*3";
	int sum=a[0]-'0';
	for(int i=1;i<strlen(a);i+=2)
	{
		if(a[i]=='*')
		{
			int b=a[i+1]-'0';
			for(i+=2;i<strlen(a);i+=2)
			{
				if(a[i]=='*')
				{
					b=b*(a[i+1]-'0');
				}
				if(a[i]=='/')
				{
					b=b/(a[i+1]-'0');
				}
				if(a[i]=='+'||a[i]=='-')
				{
					i-=2;
					break;
				}
				sum=sum*b;
			}
		}
		else if(a[i]=='/')
		{
			int b=a[i+1]-'0';
			for(i+=2;i<strlen(a);i+=2)
			{
				if(a[i]=='*')
				{
					b=b*(a[i+1]-'0');
				}
				if(a[i]=='/')
				{
					b=b/(a[i+1]-'0');
				}
				if(a[i]=='+'||a[i]=='-')
				{
					i-=2;
					break;
				}
				sum=sum/b;
			}
		}
		else if(a[i]=='+')
		{
			int b=a[i+1]-'0';
			for(i+=2;i<strlen(a);i+=2)
			{
				if(a[i]=='*')
				{
				    b=b*(a[i+1]-'0');
				}
				if(a[i]=='/')
				{
				    b=b/(a[i+1]-'0');
				} 
				if(a[i]=='+'||a[i]=='-')
				{
					i-=2;
					break;
				}
			}
			sum=sum+b;
		}
		else if(a[i]=='-')
		{
			int b=a[i+1]-'0';
			for(i+=2;i<strlen(a);i+=2)
			{
				if(a[i]=='*')
				{
				    b=b*(a[i+1]-'0');
				}
				if(a[i]=='/')
				{
				    b=b/(a[i+1]-'0');
				} 
			    if(a[i]=='+'||a[i]=='-')
				{
					i-=2;
					break;
				}
			}
			sum=sum-b;
		}
	 } 
	 printf("%d",sum);
	 return 0;
