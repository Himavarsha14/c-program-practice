
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
## 6.Program to check whether a string is palindrome or not
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
## 7.Program to count vowels, consonants, digits, and spaces in a given string
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
        char str[100];
        int vowels=0,consonants=0,digits=0,spaces=0;
        printf("Enter the string:\n");
        fgets(str,100,stdin);
        str[strcspn(str, "\n")]='\0';
        for(int i=0;str[i]!='\0';i++)
        {
                char ch=tolower(str[i]);
                if(isalpha(ch))
                {
                        if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u')
                        {
                                vowels++;
                        }
                        else
                        {
                                consonants++;
                        }
                }
                else if(ch>='0' && ch<='9')
                {
                        digits++;
                }
                else if(ch==' ')
                {
                        spaces++;
                }
        }
        printf("Vowels:%d\n",vowels);
        printf("consonants:%d\n",consonants);
        printf("digits:%d\n",digits);
        printf("spaces:%d\n",spaces);
        return 0;
}
```
## 8.Program to Concatenate two strings without using strcat()
```c
#include<stdio.h>
#include<string.h>
int main()
{       char str1[100],str2[100];
        printf("Enter string 1:\n");
        fgets(str1,100,stdin);
        str1[strcspn(str1,"\n")]='\0';
        printf("Enter string 2:\n");
        fgets(str2,100,stdin);
        str2[strcspn(str2,"\n")]='\0';
        int len1=strlen(str1);
        int len2=strlen(str2);
        for(int i=0;i<=len2;i++)
        {
                str1[len1+i]=str2[i];
        }
        printf("Concatenated string:%s\n",str1);
        return 0;
}
```
## 9.Program to Count Frequency of each character in a string
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
#define SIZE 256
int main()
{
        char str[100];
        printf("Enter a sting:\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        int freq[SIZE]={0};
        char ch;
        for(int i=0;str[i]!='\0';i++)
        {
                ch=tolower(str[i]);
                if(str[i]!=' ')
                {
                        freq[ch]++;
                }
        }
        for(int i=0;i<SIZE;i++)
        {
                if(freq[i]>0)
                {
                        printf("%c:%d\n",i,freq[i]);
                }
        }
        return 0;
}

```
## 10.Program to check strings are anagram or not
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
#define SIZE 256
int main()
{
        char str1[100],str2[100];
        printf("Enter first string:\n");
        fgets(str1,100,stdin);
        str1[strcspn(str1,"\n")]='\0';
        printf("Enter second string:\n");
        fgets(str2,100,stdin);
        str2[strcspn(str2,"\n")]='\0';
        char freq1[SIZE]={0};
        char freq2[SIZE]={0};
        int i;
        char ch;
        int flag=1;
        for(i=0;str1[i]!='\0';i++)
        {
                ch=tolower(str1[i]);
                if(isalnum(ch))
                {
                        freq1[ch]++;
                }
        }
        for(i=0;str2[i]!='\0';i++)
        {
                ch=tolower(str2[i]);
                if(isalnum(ch))
                {
                        freq2[ch]++;
                }
        }
        for(i=0;i<SIZE;i++)
        {
                if(freq1[i]!=freq2[i])
                {
                        flag=0;
                        break;
                }
        }
        if(flag)
        {
                printf("Both the strings are anagrams\n");
        }
        else
        {
                printf("Both the strings are not  anagrams\n");
        }
        return 0;
}
```
## 11. Program to find the longest word in a sentence
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    printf("Enter a string:\n");
    fgets(str,sizeof(str),stdin);
    str[strcspn(str, "\n")] = '\0';
    int curr_len=0;
    int max_len=0;
    int curr_start=0;
    int max_start=0;
    for(int i=0;str[i]!='\0';i++)
    {
        if(str[i]!=' '&& str[i]!='\n')
        {
        if(curr_len==0)
        {
            curr_start=i;
        }
        curr_len++;
        }
        else
        {
            if(curr_len>max_len)
            {
                max_len=curr_len;
                max_start=curr_start;
            }
            curr_len=0;
        }
    }
    if(curr_len>max_len)
    {
        max_len=curr_len;
        max_start=curr_start;
    }
    printf("Longest word is:");
    for(int i=max_start;i<max_start+max_len;i++)
    {
        printf("%c",str[i]);
    }
    printf("\nLength:%d",max_len);
    return 0;
}
```


