#include<stdio.h>
#include<stdlib.h>
#include<conio.h>
int main(void)
{
    FILE *fpa;
    FILE *fpb;
    int ch,key;
    if(getch()=='-e')
        {
            fpa=fopen("f:\\letter.txt","r");
    while(getch()=='1234')
        {
            fpb=fopen("f:\\encrypted.txt","w");
            while(1)
                ch=fgetc(fpa);
            if(feof(fpa))
                break;
            ch^=key;
            fputc(ch,fpb);
            }
            fclose(fpa);
            fclose(fpb);
            }
            while(getch()=='-o')
                {
                    fpa=fopen("f:\\encrypted.txt","r");
                    fpb=fopen("f:\\LOL.txt","w");
                    while(1){
                            ch=fgetc(fpa);
                    if(feof(fpa))
                        break;
                    ch^=key;
                    fputc(ch,fpb);
                    }
                    fclose(fpa);
                    fclose(fpb);
                    return 0;
                    }
}
