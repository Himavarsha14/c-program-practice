## 1.WRITE A C PROGRAM TO ACCEPT TWO INTEGERS AND CHECK WHETHER THEY ARE EQUAL OR NOT
```c
#include<stdio.h>
int main()
{
    int a,b;
    printf("Enter the value of a and b:\n");
    scanf("%d %d",&a,&b);
    if(a==b)
    {
        printf("%d and %d are equal\n",a,b);
    }
    else
    {
        printf("%d and %d are not equal\n",a,b);
    }
    return 0;
}
```
## 2.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS EVEN OR ODD
```c
#include<stdio.h>
int main()
{
    int num;
    printf("Enter a number:\n");
    scanf("%d",&num);
    if(num%2==0)
    {
        printf("The given number %d is an even number.\n",num);
    }
    else
    {
        printf("The given number %d is an odd number.\n",num);
    }
}
```
## 3.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS POSITIVE OR NEGATIVE
```c
#include<stdio.h>
int main()
{
    int num;
    printf("Enter a number:\n");
    scanf("%d",&num);
    if(num>0)
    {
        printf("The given number %d is a positive number.\n",num);
    }
    else
    {
        printf("The given number %d is a negative number.\n",num);
    }
}
```
## 4.WRITE A C PROGRAM TO FIND WHETHER A GIVEN YEAR IS A LEAP YEAR OR NOT?
```c
#include<stdio.h>
int main()
{
    int year;
    printf("Enter a year:\n");
    scanf("%d",&year);
    if(year%4==0 && year%100!=0 || year%400==0)
    {
        printf("The given year %d is a leap year.\n",year);
    }
    else
    {
        printf("The given year %d is not a leap year.\n",year);
    }
}
```
## 5.WRITE A C PROGRAM TO READ THE AGE OF A CANDIDATE AND DETERMINE WHETHER HE IS ELIGIBLE TO CAST HIS/HER OWN VOTE
```c
#include<stdio.h>
int main()
{
    int age;
    printf("Enter age:\n");
    scanf("%d",&age);
    if(age<=0)
    {
    printf("Enter valid age\n");
    }
    else if(age>18)
    {
        printf("The person is eligible to cast his/her vote\n");
    }
    else
    {
        printf("The person is not eligible to cast his/her vote\n");;
    
    }
    return 0;
}
```
