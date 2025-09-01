## 1.Which is not a bitwise operator?
1. &
2. |
3. <<
4. &&
Ans:option 4:It is logical AND operator.
## 2.Predict the output of the following program.
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
Ans:c=2
## 3.Predict the output of the following program.
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
## 4.Predict the output of the following program.
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
Ans:4,5
## 5.Predict the output of the following program.
#include <stdio.h>
int main()
{
char flag=0x0f;
flag &= ~0x02;
printf("%d",flag);
return 0;
}
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









