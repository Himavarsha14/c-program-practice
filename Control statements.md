<img width="225" height="225" alt="image" src="https://github.com/user-attachments/assets/35e0a120-dd5c-4cdc-8677-ece816831a38" />## 1.WRITE A C PROGRAM TO ACCEPT TWO INTEGERS AND CHECK WHETHER THEY ARE EQUAL OR NOT
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
## 22.Program to Print a pattern of stars using nested loops
```c
#include <stdio.h>

int main() {
    int n, i, j;
    printf("Enter number of rows: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }
    return 0;
}
```
## 23.WRITE A C PROGRAM TO SEARCH FOR AN ELEMENT IN AN ARRAY USING LINEAR SEARCH AND A FOR LOOP.
```c
#include <stdio.h>

int main() {
    int n, i, key, found = 0;
    printf("Enter size of array: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++)
        scanf("%d", &arr[i]);
    printf("Enter element to search: ");
    scanf("%d", &key);
    for (i = 0; i < n; i++) {
        if (arr[i] == key) {
            printf("Element found at position %d\n", i + 1);
            found = 1;
            break;
        }
    }
    if (!found)
        printf("Element not found.\n");
    return 0;
}
```
## 24.Program to check whether given number is Palindrome in decimal & binary.
```c
#include <stdio.h>
int isPalindrome(int num) {
    int rev = 0, temp = num;
    while (temp > 0) {
        rev = rev * 10 + temp % 10;
        temp /= 10;
    }
    return (rev == num);
}
int isBinaryPalindrome(int num) {
    int bin[32], i = 0, j;
    while (num > 0) {
        bin[i++] = num % 2;
        num /= 2;
    }
    for (j = 0; j < i / 2; j++) {
        if (bin[j] != bin[i - j - 1])
            return 0;
    }
    return 1;
}
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    if (isPalindrome(n))
        printf("%d is a decimal palindrome.\n", n);
    else
        printf("%d is not a decimal palindrome.\n", n);
    if (isBinaryPalindrome(n))
        printf("Its binary representation is also palindrome.\n");
    else
        printf("Its binary representation is not palindrome.\n");
    return 0;
}
```
## 25.WRITE A C PROGRAM TO FIND THE SUM OF FIRST N NATURAL NUMBERS WHICH ARE NOT DIVISIBLE BY 3 OR 5 USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main() {
    int n, i, count = 0, sum = 0;
    printf("Enter N: ");
    scanf("%d", &n);
    for (i = 1; count < n; i++) {
        if (i % 3 != 0 && i % 5 != 0) {
            sum += i;
            count++;
        }
    }
    printf("Sum = %d\n", sum);
    return 0;
}
```
## 26.WRITE A C PROGRAM TO FIND THE SUM OF ALL EVEN NUMBERS BETWEEN TWO GIVEN NUMBERS USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main() {
    int a, b, i, sum = 0;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    for (i = a; i <= b; i++) {
        if (i % 2 == 0)
            sum += i;
    }
    printf("Sum of even numbers = %d\n", sum);
    return 0;
}
```
## 27.WRITE A C PROGRAM TO FIND THE SUM OF ALL ODD NUMBERS BETWEEN TWO GIVEN NUMBERS USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main() {
    int a, b, i, sum = 0;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    for (i = a; i <= b; i++) {
        if (i % 2 != 0)
            sum += i;
    }
    printf("Sum of odd numbers = %d\n", sum);
    return 0;
}
```
## 28.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS A PERFECT SQUARE OR NOT USING LOOPS AND IF-ELSE STATEMENTS.
```c
#include <stdio.h>
int main() {
    int n, i, flag = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (i = 1; i * i <= n; i++) {
        if (i * i == n) {
            flag = 1;
            break;
        }
    }
    if (flag)
        printf("%d is a perfect square.\n", n);
    else
        printf("%d is not a perfect square.\n", n);
    return 0;
}
```
## 29.WRITE A C PROGRAM TO CALCULATE THE POWER OF A NUMBER USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main() {
    int base, exp, i;
    long long result = 1;
    printf("Enter base and exponent: ");
    scanf("%d %d", &base, &exp);
    for (i = 1; i <= exp; i++) {
        result *= base;
    }
    printf("%d^%d = %lld\n", base, exp, result);
    return 0;
}
```
## 30.WRITE A C PROGRAM TO FIND THE ASCII VALUE OF A CHARACTER USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main() {
    char c;
    printf("Enter a character: ");
    scanf(" %c", &c);
    printf("ASCII value of %c = %d\n", c, c);
    return 0;
}
```
## 31.WRITE A C PROGRAM TO FIND THE AREA OF A CIRCLE GIVEN ITS RADIUS USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main() {
    float r, area;
    printf("Enter radius: ");
    scanf("%f", &r);
    if (r > 0) {
        area = 3.14159 * r * r;
        printf("Area = %.2f\n", area);
    } else {
        printf("Invalid radius.\n");
    }
    return 0;
}
```
## 32.WRITE A C PROGRAM TO FIND THE SUM OF ALL PRIME NUMBERS BETWEEN 1 AND 1000 USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>
int main() {
    int i, j, sum = 0, prime;
    for (i = 2; i <= 1000; i++) {
        prime = 1;
        for (j = 2; j * j <= i; j++) {
            if (i % j == 0) {
                prime = 0;
                break;
            }
        }
        if (prime)
            sum += i;
    }
    printf("Sum of primes between 1 and 1000 = %d\n", sum);
    return 0;
}
```
## 33.WRITE A C PROGRAM TO PRINT THE PATTERN OF STARS IN A HOLLOW SQUARE SHAPE USING LOOPS AND IF-ELSE STATEMENTS?
```c
#include <stdio.h>

int main() {
    int n, i, j;
    printf("Enter the size of square: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= n; j++) {
            if (i == 1 || i == n || j == 1 || j == n)
                printf("* ");
            else
                printf("  ");
        }
        printf("\n");
    }
    return 0;
}
```
## 34.Program to print right triangle of stars
```c
#include <stdio.h>
int main() {
    int n, i, j;
    printf("Enter number of rows: ");
    scanf("%d", &n);

    for (i = 1; i <= n; i++) {
        for (j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }
    return 0;
}
```
## 35.Program to print mirror right triangle of stars
```c
#include <stdio.h>
int main() {
    int n, i, j;
    printf("Enter number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= n; j++) {
            if (j <= n - i)
                printf("  ");
            else
                printf("* ");
        }
        printf("\n");
    }
    return 0;
}
```
## 36.Program to print diamond of stars
```c
#include <stdio.h>
int main() {
    int n, i, j, k;
    printf("Enter number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= n - i; j++) 
        {
            printf(" ");
        }
        for (k = 1; k <= (2*i - 1); k++)
        {
            printf("*");
        }
        printf("\n");
    }
    return 0;
}
```
## 37.Program to print hollow diamond
```c
#include <stdio.h>
int main() {
    int n, i, j;
    printf("Enter number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= n - i; j++) printf(" ");
        for (j = 1; j <= 2*i - 1; j++) {
            if (j == 1 || j == 2*i - 1) printf("*");
            else printf(" ");
        }
        printf("\n");
    }
    for (i = n - 1; i >= 1; i--) {
        for (j = 1; j <= n - i; j++) printf(" ");
        for (j = 1; j <= 2*i - 1; j++) {
            if (j == 1 || j == 2*i - 1) printf("*");
            else printf(" ");
        }
        printf("\n");
    }
    return 0;
}
```
## 38.Program to print number pyramid
```c
#include <stdio.h>
int main() {
    int n, i, j, k;
    printf("Enter number of rows: ");
    scanf("%d", &n);
    for (i = 1; i <= n; i++) {
        for (j = 1; j <= n - i; j++) printf(" ");
        for (k = 1; k <= (2*i - 1); k++) printf("%d", i);
        printf("\n");
    }
    return 0;
}
```
## 39.Program to print mirrored number pyramid
```c
#include <stdio.h>
int main() {
    int n, i, j, k;
    printf("Enter number of rows: ");
    scanf("%d", &n);

    for (i = n; i >= 1; i--) {
        for (j = 1; j <= n - i; j++) printf(" ");
        for (k = 1; k <= 2*i - 1; k++) printf("%d", i);
        printf("\n");
    }
    return 0;
}
```

























