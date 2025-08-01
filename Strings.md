
## 1.Program to find the length of the string without using library functions
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
## 5.Program to check whether a string is palindrome or not
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
## 6.Program to count vowels, consonants, digits, and spaces in a given string
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
## 7.Program to Concatenate two strings without using strcat()
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
## 8.Program to Count Frequency of each character in a string
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
## 9.Program to check strings are anagram or not
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
## 10. Program to find the longest word in a sentence
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
## 11.Find the length of the last word in a string 
```c
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int count = 0;
    fgets(str, 100, stdin);                             // 1. Reads input including spaces
    str[strcspn(str, "\n")] = '\0';                     // 2. Removes newline character from input

    int length = strlen(str);                           // 3. Finds the length of the string
    int i;

    // 4. FOR LOOP 1: Skip trailing spaces from the end of the string
    for (i = length - 1; i >= 0 && str[i] == ' '; i--);
    // Now, i points to the last character of the last word

    // 5. FOR LOOP 2: Count characters in the last word
    for (; i >= 0 && str[i] != ' '; i--) {
        count++;
    }

    // 6. Print the result
    printf("%d\n", count);
    return 0;
}
```
## 12.C program to check if string is pangram or not.
```c
#include<stdio.h>
#include<string.h>
#include<ctype.h>
void panagram(char str[])
{
    int found;
    for(char ch='a';ch<='z';ch++)
    {
        found=0;
        for(int i=0;str[i]!='\0';i++)
        {
            if(ch==str[i])
            {
                found=1;
                break;
            }
        }
        if(found==0)
        {
            printf("Not panagram\n");
            return;
        }
    }
    printf("panagram\n");
}
int main()
{
    char str[1000];
    fgets(str,1000,stdin);
    str[strcspn(str,"\n")]='\0';
    for(int i=0;str[i]!='\0';i++)
    {
        str[i]=tolower(str[i]);
    }
    panagram(str);
    return 0;
}

```
## 13.Program to print sum of digits in a string
```c
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    printf("Enter a string:\n");
    fgets(str,100,stdin);
    str[strcspn(str,"\n")]='\0';
    int sum=0;
    for(int i=0;str[i]!='\0';i++)
    {
        if(str[i]>='0'&&str[i]<='9')
        {
            sum=sum+(str[i]-'0');
        }
    }
    printf("The sum of digits in the string are:%d\n",sum);
    return 0;
}
```
## 14.Program to count and list substrings of a string
```c
#include<stdio.h>
#include<string.h>
int main()
{
        char str[100];
        printf("Enter a substring:\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        int len=strlen(str);
        int count=0;
        int i,j,k;
        printf("The substrings are:\n");
        for(i=0;i<len;i++)
        {
                for(j=i;j<len;j++)
                {
                        for(k=i;k<=j;k++)
                        {
                                printf("%c",str[k]);
                        }
                        printf("\n");
                        count++;
                }
        }
        printf("The number of substrings are:%d'\n",count);
        return 0;
}
```
## 15.Program to append two strings using DMA calls
```c
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
        char *str,*append;
        str=(char *)malloc(100*sizeof(char));
        if(str==NULL)
        {
                printf("Malloc error\n");
                return 1;
        }
        printf("Enter inital string:\n");
        scanf("%s",str);
        append=(char *)malloc(100* sizeof(char));
        if(append==NULL)
        {
                printf("Malloc error\n");
                return 1;
        }
        printf("Enter a string:\n");
        scanf("%s",append);
        char *str1;
        str1=(char *)realloc(str,strlen(str)+strlen(append)+1);
        if(str1==NULL)
        {
                printf("realloc error\n");
                free(str);
                free(append);
                return 1;
        }

        str=str1;
        strcat(str,append);
        printf("new string:%s\n",str);
        free(str);
        return 0;
}
```
## 16.Program to find whether a substring is present in a string or not
```c
#include<stdio.h>
#include<string.h>
int main()
{
        char str[100];
        printf("Enter a string:\n");
        fgets(str,100,stdin);
        str[strcspn(str,"\n")]='\0';
        char substr[20];
        printf("Enter substring:\n");
        fgets(substr,20,stdin);
        substr[strcspn(substr,"\n")]='\0';
        int len=strlen(str);
        int sublen=strlen(substr);
        int found=0;
        for(int i=0;i<=len-sublen;i++)
        {
        int j;
        for(j=0;j<sublen;j++)
        {
        if(str[i+j]!=substr[j])
        {
        break;
        }
        }
        if(j==sublen)
        {
        found=1;
        break;
        }
        }
if(found==1)
{
printf("The substring is present\n");
}
else
{
        printf("The substring is not present:\n");
}
return 0;
}
```

