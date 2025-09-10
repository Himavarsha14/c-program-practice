## 1.Which is not a bitwise operator?
1. &
2. |
3. <<
4. &&
Ans:option 4:It is logical AND operator.
## 2.Predict the output of the following program.
```c
#include <stdio.h>
int main()
{
int a=10;
int b=2;
int c;
c=(a & b);
printf("c= %d",c);
return 0;
}
```
Ans:c=2
## 3.Predict the output of the following program.
```c
#include <stdio.h>
#define MOBILE 0x01
#define LAPPY 0x02
int main()
{
unsigned char item=0x00;
item |=MOBILE;
item |=LAPPY;
printf("I have purchased ...:");
if(item & MOBILE){
printf("Mobile, ");
}
if(item & LAPPY){
printf("Lappy");
}
return 1;
}
Ans:#include <stdio.h>
#define MOBILE 0x01
#define LAPPY 0x02
int main()
{
unsigned char item=0x00;
item |=MOBILE;
item |=LAPPY;
printf("I have purchased ...:");
if(item & MOBILE){
printf("Mobile, ");
}
if(item & LAPPY){
printf("Lappy");
}
return 1;
}
```
## 4.Predict the output of the following program.
```c
#include <stdio.h>
int main()
{
char var=0x04;
var = var | 0x04;
printf("%d,",var);
var |= 0x01;
printf("%d",var);
return 0;
}
```
Ans:4,5
## 5.Predict the output of the following program.
```c
#include <stdio.h>
int main()
{
char flag=0x0f;
flag &= ~0x02;
printf("%d",flag);
return 0;
}
```
Ans:13
## 6.Toggle a given range of bitsFor example, take the number 245. The equivalent binary format is 11110101and the range is to 7. So, the output should be 000001010 which is 5 in decimal.
```c
#include <stdio.h>
int main() {
    int num = 245;    // 11110101
    int l = 4, r = 7; //range

    int mask = ((1 << (r - l + 1)) - 1) << (l - 1);
    int ans = num ^ mask;

    printf("%d\n", ans); // Output: 5
    return 0;
}
```
## 7.How to check if a particular bit is set or not in a number?
```c
#include <stdio.h>
int main() {
    int num = 10; // 1010
    int pos = 2;  // check 2nd bit (from LSB = 1)

    if (num & (1 << (pos - 1)))
        printf("Bit is SET\n");
    else
        printf("Bit is NOT set\n");

    return 0;
}
```
## 8.Find whether the number is odd or even
```c
#include <stdio.h>
int main() {
    int num = 15;
    if (num & 1)
        printf("Odd\n");
    else
        printf("Even\n");
    return 0;
}
```
## 9.Clear the last right side set a bit of a number
```c
#include <stdio.h>
int main() {
    int num = 12; // 1100
    num = num & (num - 1);
    printf("%d\n", num); // Output: 8
    return 0;
}
```
## 10.Check if the number is a power of 2
```c
#include <stdio.h>
int main() {
    int num = 16;
    if (num > 0 && (num & (num - 1)) == 0)
        printf("Power of 2\n");
    else
        printf("Not Power of 2\n");
    return 0;
}
```
## 11.Count the number of set bits in a number
```c
#include <stdio.h>
int main() {
    int num = 29; // 11101
    int count = 0;
    while (num) {
        count += num & 1;
        num >>= 1;
    }
    printf("Set bits = %d\n", count); // 4
    return 0;
}
```
## 12.Swap two bits at given positions
```c
#include <stdio.h>
int main() {
    int num = 28; // 11100
    int pos1 = 2, pos2 = 5;

    int bit1 = (num >> (pos1 - 1)) & 1;
    int bit2 = (num >> (pos2 - 1)) & 1;

    if (bit1 != bit2) {
        num ^= (1 << (pos1 - 1));
        num ^= (1 << (pos2 - 1));
    }

    printf("%d\n", num);
    return 0;
}
```
## 13.Implement a C program to count the number of bits that need to be flipped to convert integer A to integer B using bitwise operators.
```c
#include <stdio.h>

int main() {
    int A, B;
    printf("Enter two numbers: ");
    scanf("%d %d", &A, &B);

    int xor = A ^ B;  // XOR shows differing bits
    int count = 0;

    while (xor) {
        count += xor & 1; // check last bit
        xor >>= 1;        // shift right
    }

    printf("Number of bits to flip: %d\n", count);
    return 0;
}
```
## 14.Write a C program to set odd position bits
```c#include <stdio.h>

int main() {
    unsigned int n;
    printf("Enter a number: ");
    scanf("%u", &n);

    n |= 0xAAAAAAAA; 
    printf("After setting odd bits: %u\n", n);

    return 0;
}
```
## 15.Count number of set bits in sum of two numbers
```c
#include <stdio.h>
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    int sum = a + b;
    int count = 0;
    while (sum) {
        count += sum & 1;
        sum >>= 1;
    }
    printf("Set bits in sum: %d\n", count);
    return 0;
}
```
## 16.MACRO to swap bytes in 16 bit integer variable
```c
#include <stdio.h>
#include <stdint.h>

#define SWAP16(x) ( ((x & 0x00FF) << 8) | ((x & 0xFF00) >> 8) )

int main() {
    uint16_t a = 0x1234;  // Example number
    printf("Original: 0x%04X\n", a);
    printf("Swapped : 0x%04X\n", SWAP16(a));
    return 0;
}
```
## 17.MACRO to swap bytes in 32 bit integer variable
```c
#include <stdio.h>
#include <stdint.h>

#define SWAP32(x) ( ((x & 0x000000FF) << 24) | \
                    ((x & 0x0000FF00) << 8)  | \
                    ((x & 0x00FF0000) >> 8)  | \
                    ((x & 0xFF000000) >> 24) )
int main() {
    uint32_t b = 0x12345678;  // Example number
    printf("Original: 0x%08X\n", b);
    printf("Swapped : 0x%08X\n", SWAP32(b));
    return 0;
}
```
## 18.Write a program that enters temperature in Celsius and converts that into Fahrenheit.
```c
#include <stdio.h>
int main() {
    float celsius, fahrenheit;
    printf("Enter temperature in Celsius: ");
    scanf("%f", &celsius);
    fahrenheit = (celsius * 9 / 5) + 32;
    printf("%.2f Celsius = %.2f Fahrenheit\n", celsius, fahrenheit);
    return 0;
}
```
## 19.Write a program that accepts the radius of a circle and calculates the area and perimeter of that circle.
```c
#include <stdio.h>
#define PI 3.14159
int main() {
    float radius, area, perimeter;
    printf("Enter radius of circle: ");
    scanf("%f", &radius);
    area = PI * radius * radius;
    perimeter = 2 * PI * radius;
    printf("Area = %.2f\n", area);
    printf("Perimeter = %.2f\n", perimeter);

    return 0;
}
```
## 20.Write a program to accept a number in decimal and print the number in octal and hexadecimal.
```c
#include <stdio.h>
int main() {
    int num;
    printf("Enter a decimal number: ");
    scanf("%d", &num);
    printf("Octal: %o\n", num);
    printf("Hexadecimal: %X\n", num);
    return 0;
}
```
## 21.Write a program to accept any number and print the value of remainder after dividing it by 3.
```c
#include <stdio.h>
int main() {
    int num, remainder;
    printf("Enter a number: ");
    scanf("%d", &num);
    remainder = num % 3;
    printf("Remainder after dividing %d by 3 = %d\n", num, remainder);
    return 0;
}
```
## 22.Write a program that accepts marks in five subjects and calculates the total percentage marks.
```c
#include <stdio.h>
int main() {
    float marks[5];
    float total = 0, percentage;
    int i;
    for(i = 0; i < 5; i++) {
        printf("Enter marks for subject %d: ", i+1);
        scanf("%f", &marks[i]);
    }
    for(i = 0; i < 5; i++) {
        total += marks[i];
    }
    percentage = (total / 500) * 100;  // assuming each subject is out of 100
    printf("Total Marks = %.2f\n", total);
    printf("Percentage = %.2f%%\n", percentage);
    return 0;
}
```
## 23.Write a C program that uses the bitwise operators to check if a given positive integer is divisible by both 6 and 9.
```c
#include <stdio.h>
int isDivisibleBy9(int n) {
    int sum = 0, temp = n;
    while(temp > 0) {
        sum += temp % 10;
        temp /= 10;
    }
    return (sum % 9 == 0); 
}
int main() {
    int n;
    printf("Enter a positive integer: ");
    scanf("%d", &n);
    if( (n & 1) == 0 && isDivisibleBy9(n) )
        printf("%d is divisible by both 6 and 9\n", n);
    else
        printf("%d is NOT divisible by both 6 and 9\n", n);
    return 0;
}
```
## 24.Implement a program that checks if a number is less than 50 without using the less than operator.
```c
#include<stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    int diff=50-n;
    if((diff>>31)==0)
    {
         printf("It is a positive number");
    }
    else
    {
        printf("it is negative number");
    }
}
```

















