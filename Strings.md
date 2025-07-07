###
1.Program to find the lenghth of the string without using library functios
#include<stdio.h>
#include<string.h>
int main()
{
        char str[100];
        int count=0;
        printf("Enter a string\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        printf("The length of the string is:");
        for(int i=0;str[i]!='\0';i++)
        {
                count++;
        }
        printf("%d",count);
        printf("\n");
        return 0;
}

