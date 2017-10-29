#include <stdio.h>
#include <string.h>
int main(void)
{
	FILE *file1,*file2;
	int now;
	int paslen;
	char a;
	char b[50];
	char c[]="-e";
	char d[]="-o";
	char key[50];
	scanf("%s",b);
	getchar();
	if(strcmp(b,c)==0)
	{
		gets(key);
		paslen=strlen(key);
		file1=fopen("f:\\baidu\\letter.txt","rb");
		file2=fopen("f:\\baidu\\encrypted.txt","wb+");
		a=fgetc(file1);
        now=0;
		while(a!=EOF)
		{
			a=a^(key[now++]);
			fputc(a,file2);
			a=fgetc(file1);
		}
		fclose(file1);
		fclose(file2);
	}
	if(strcmp(b,d)==0)
	{
		gets(key);
		paslen=strlen(key);
		file1=fopen("f:\\baidu\\encrypted.txt","rb");
		file2=fopen("f:\\baidu\\final.txt","wb+");
		a=fgetc(file1);
		now=0;
		while(a!=EOF)
		{
			a=a^(key[now++]);
			fputc(a,file2);
			a=fgetc(file1);
		}
		fclose(file1);
		fclose(file2);
	}
	return 0;
}
