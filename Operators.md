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
