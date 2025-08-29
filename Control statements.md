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
## 6.WRITE A C PROGRAM TO READ THE VALUE OF AN INTEGER M AND DISPLAY THE VALUE OF N IS 1 WHEN M IS LARGER THAN 0, 0 WHEN M IS 0 AND -1 WHEN M IS LESS THAN 0.
```c
#include <stdio.h>
int main() {
    int m, n;
    printf("Enter value of M: ");
    scanf("%d", &m);
    if (m > 0) n = 1;
    else if (m == 0) n = 0;
    else n = -1;
    printf("Value of N = %d\n", n);
    return 0;
}
```
## 7.WRITE A C PROGRAM TO FIND THE LARGEST OF THREE NUMBERS
```c
#include <stdio.h>
int main() {
    int a, b, c;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    if (a >= b && a >= c) printf("Largest = %d\n", a);
    else if (b >= a && b >= c) printf("Largest = %d\n", b);
    else printf("Largest = %d\n", c);
    return 0;
}
```
## 8.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS A VOWEL OR CONSONANT
```c
#include <stdio.h>
int main() {
    char ch;
    printf("Enter a character: ");
    scanf(" %c", &ch);
    if (ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U')
        printf("%c is a Vowel\n", ch);
    else
        printf("%c is a Consonant\n", ch);
    return 0;
}
```
## 9.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS AN ALPHABET OR NOT
```c
#include <stdio.h>
int main() {
    char ch;
    printf("Enter a character: ");
    scanf(" %c", &ch);
    if ((ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z'))
        printf("%c is an Alphabet\n", ch);
    else
        printf("%c is Not an Alphabet\n", ch);
    return 0;
}
```
## 10.WRITE A C PROGRAM TO FIND MINIMUM OR MAXIMUM BETWEEN TWO NUMBERS
```c
#include <stdio.h>
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    if (a > b) printf("Max = %d, Min = %d\n", a, b);
    else printf("Max = %d, Min = %d\n", b, a);
    return 0;
}
```
## 11.WRITE A C PROGRAM TO ENTER WEEK NUMBER AND PRINT DAY OF WEEK
```c
#include <stdio.h>
int main() {
    int n;
    printf("Enter week number (1-7): ");
    scanf("%d", &n);
    switch (n) {
        case 1: printf("Sunday\n"); break;
        case 2: printf("Monday\n"); break;
        case 3: printf("Tuesday\n"); break;
        case 4: printf("Wednesday\n"); break;
        case 5: printf("Thursday\n"); break;
        case 6: printf("Friday\n"); break;
        case 7: printf("Saturday\n"); break;
        default: printf("Invalid week number\n");
    }
    return 0;
}
```
## 12.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS UPPERCASE OR LOWERCASE
```c
#include <stdio.h>
int main() {
    char ch;
    printf("Enter a character: ");
    scanf(" %c", &ch);
    if (ch >= 'A' && ch <= 'Z') printf("%c is Uppercase\n", ch);
    else if (ch >= 'a' && ch <= 'z') printf("%c is Lowercase\n", ch);
    else printf("%c is Not an Alphabet\n", ch);
    return 0;
}
```
## 13.WRITE A C PROGRAM TO FIND NUMBER OF DAYS IN MONTH
```c
#include <stdio.h>
int main() {
    int month;
    printf("Enter month number (1-12): ");
    scanf("%d", &month);
    switch (month) {
        case 1: case 3: case 5: case 7: case 8: case 10: case 12:
            printf("31 days\n"); break;
        case 4: case 6: case 9: case 11:
            printf("30 days\n"); break;
        case 2:
            printf("28 or 29 days\n"); break;
        default:
            printf("Invalid month\n");
    }
    return 0;
}
```
## 14.WRITE A C PROGRAM TO FIND MAXIMUM BETWEEN TWO NUMBERS USING SWITCH CASE
```c
#include <stdio.h>
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    switch (a > b) {
        case 1: printf("Maximum = %d\n", a); break;
        case 0: printf("Maximum = %d\n", b); break;
    }
    return 0;
}
```
## 15.WRITE A C PROGRAM TO PRINT EVEN NUMBERS BETWEEN 1 TO 20 USING A FOR LOOP
```c
#include <stdio.h>
int main() {
    printf("Even numbers between 1 to 20:\n");
    for (int i = 1; i <= 20; i++)
        if (i % 2 == 0)
           printf("%d ", i);
    return 0;
}
```
## 16.WRITE A C PROGRAM TO CALCULATE THE SUM OF NUMBERS FROM 1 TO 100 USING A WHILE LOOP
```c
#include <stdio.h>
int main() {
    int i = 1, sum = 0;
    while (i <= 100) {
        sum += i;
        i++;
    }
    printf("Sum = %d\n", sum);
    return 0;
}
```
## 17.WRITE A C PROGRAM TO FIND THE FACTORIAL OF A GIVEN NUMBER USING A FOR LOOP
```c
#include <stdio.h>
int main() {
    int n, fact = 1;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        fact *= i;
    }
    printf("Factorial = %d\n", fact);
    return 0;
}
```
## 18.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS PRIME OR NOT USING A WHILE LOOP
```c
#include <stdio.h>
int main() {
    int n, i = 2, flag = 1;
    printf("Enter a number: ");
    scanf("%d", &n);
    if (n <= 1) flag = 0;
    while (i <= n / 2) {
        if (n % i == 0) {
            flag = 0;
            break;
        }
        i++;
    }
    if (flag) printf("%d is Prime\n", n);
    else printf("%d is Not Prime\n", n);
    return 0;
}
```
## 19.WRITE A C PROGRAM TO FIND THE SUM OF DIGITS OF A NUMBER USING A WHILE LOOP
```c
#include <stdio.h>
int main() {
    int n, sum = 0, digit;
    printf("Enter a number: ");
    scanf("%d", &n);
    while (n > 0) {
        digit = n % 10;
        sum += digit;
        n /= 10;
    }
    printf("Sum of digits = %d\n", sum);
    return 0;
}
```
## 20.WRITE A C PROGRAM TO PRINT FIBONACCI SERIES UP TO N TERMS USING A FOR LOOP
```c
#include <stdio.h>
int main() {
    int n, a = 0, b = 1, c;
    printf("Enter number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci Series: ");
    for (int i = 1; i <= n; i++) {
        printf("%d ", a);
        c = a + b;
        a = b;
        b = c;
    }
    return 0;
}
```
## 21.WRITE A C PROGRAM TO REVERSE A GIVEN NUMBER USING A WHILE LOOP?
```c
#include <stdio.h>
int main() {
    int n, rev = 0, digit;
    printf("Enter a number: ");
    scanf("%d", &n);
    while (n > 0) {
        digit = n % 10;
        rev = rev * 10 + digit;
        n /= 10;
    }
    printf("Reversed number = %d\n", rev);
    return 0;
}
```












