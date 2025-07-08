
## 1.Program to find the lenghth of the string without using library functions
```c

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
```
## 2.Program to seperate individual characters from a string
```c
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
```
## 3.Program to print individual characters of a string in reverse order
```c
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
```
## 4.Program to count total number of words in a string
```c
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
## 5.Program to compare two strings
```c
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
## Program to check whether a string is palindrome or not
```c
#include<stdio.h>
#include<string.h>
int main()
{
        char str[100];
        printf("Enter a string:\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        int len=strlen(str);
        int start,end,flag=0;
        start=0;
        end=len-1;
        while(start<end)
        {
                if(str[start]!=str[end])
                {
                        flag=1;
                        break;
                }
        start++;
        end--;
        }
        if(flag==0)
        {
                printf("The string is a palindrome.\n");
        }
        else
                printf("The string is not a palindrome.\n");
        return 0;
}

```

