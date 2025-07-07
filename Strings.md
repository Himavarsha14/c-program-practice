###
```c

1.Program to find the lenghth of the string without using library functions


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

2.Program to seperate individual characters from a string

#include<stdio.h>
#include<string.h>
int main()
{
        char str[100];
        printf("Enter a string:\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        int count=0;
        printf("Individual elements are:\n");
        for(int i=0;str[i]!='\0';i++)
        {
                printf("%c ",str[i]);
        }
        return 0;
}

3.Program to print individual characters of a string in reverse order

#include<stdio.h>
#include<string.h>
int main()
{
        char str[100];
        printf("Enter the string:\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        int length=strlen(str);
        for(int i=length-1;i>=0;i--)
        {
                printf("%c ",str[i]);
        }
        return 0;
}

4.Program to count total number of words in a string

#include<stdio.h>
#include<string.h>
int main()
{
        char str[100];
        printf("Enter a string:\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        int count=1;
        printf("The total number of words are:");
        for(int i=0;str[i]!='\0';i++)
        {
                if(str[i]==' '||str[i]=='\t'||str[i]=='\n')
                {
                        count++;
                }
        }
        printf("%d\n",count);
        return 0;
}

5.Program to compare two strings

#include<stdio.h>
#include<string.h>
int main()
{
        char str[100];
        printf("Enter a string:\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        int count=1;
        printf("The total number of words are:");
        for(int i=0;str[i]!='\0';i++)
        {
                if(str[i]==' '||str[i]=='\t'||str[i]=='\n')
                {
                        count++;
                }
        }
        printf("%d\n",count);
        return 0;
}




```

