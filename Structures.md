## 1.Create a structure to represent a student with the following members: name (string), roll number (int), and marks (float). Write a function to display the details of a student.
```c
#include <stdio.h>

struct Student {
    char name[50];
    int rollNo;
    float marks;
};
void displayStudent(struct Student s) {
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.rollNo);
    printf("Marks: %.2f\n", s.marks);
}
int main() {
    struct Student s = {"Himavarsha", 101, 88.5};
    displayStudent(s);
    return 0;
}
```
## 2.Define a union to store either an integer or a floatingpoint number. Write a function to accept the type of data (integer or float) and then read the corresponding value from the user. Store the value in the union and print it.
```c
#include <stdio.h>
union Data {
    int i;
    float f;
};
int main() {
    union Data d;
    int choice;
    printf("Enter 1 for Integer, 2 for Float: ");
    scanf("%d", &choice);

    if(choice == 1) {
        printf("Enter integer: ");
        scanf("%d", &d.i);
        printf("You entered integer: %d\n", d.i);
    } else {
        printf("Enter float: ");
        scanf("%f", &d.f);
        printf("You entered float: %.2f\n", d.f);
    }
    return 0;
}
```
## 3.Define a structure to represent a point in 2D space with x and y coordinates (both integers). Write a function to check if two points are equal (have the same x and y coordinates).
```c
#include <stdio.h>
struct Point {
    int x, y;
};

int areEqual(struct Point p1, struct Point p2) {
    return (p1.x == p2.x && p1.y == p2.y);
}
int main() {
    struct Point p1 = {2, 3}, p2 = {2, 3};
    if(areEqual(p1, p2))
        printf("Points are equal\n");
    else
        printf("Points are not equal\n");
    return 0;
}
```
## 4.Create a structure to represent a book with the following members: title (string), author (string), ISBN (long int), and number of pages (int). Write a function to accept details of a book from the user and store them in a structure variable.
```c
#include <stdio.h>
struct Book {
    char title[50];
    char author[50];
    long int ISBN;
    int pages;
};
int main() {
    struct Book b;
    printf("Enter title: ");
    scanf("%s", b.title);
    printf("Enter author: ");
    scanf("%s", b.author);
    printf("Enter ISBN: ");
    scanf("%ld", &b.ISBN);
    printf("Enter number of pages: ");
    scanf("%d", &b.pages);
    printf("\nBook Details:\nTitle: %s\nAuthor: %s\nISBN: %ld\nPages: %d\n",
           b.title, b.author, b.ISBN, b.pages);
    return 0;
}
```
## 5.Define a union to represent the size of a product, which can be specified in centimeters, inches, or feet. Write a function to convert the size from one unit to another (e.g., centimeters to inches).
```c
#include <stdio.h>
union Size {
    float cm, inch, feet;
};
int main() {
    union Size s;
    int choice;
    printf("Enter 1 for cm to inch, 2 for inch to feet: ");
    scanf("%d", &choice);

    if(choice == 1) {
        printf("Enter size in cm: ");
        scanf("%f", &s.cm);
        printf("In inches: %.2f\n", s.cm / 2.54);
    } else {
        printf("Enter size in inches: ");
        scanf("%f", &s.inch);
        printf("In feet: %.2f\n", s.inch / 12.0);
    }
    return 0;
}
```
## 6.Define a structure to represent a date with day, month, and year (all integers). Write a function to check if a given year is a leap year.
```c
#include <stdio.h>
struct Date {
    int day, month, year;
};

int isLeapYear(int y) {
    return ((y%4==0 && y%100!=0) || (y%400==0));
}
int main() {
    struct Date d = {1,1,2024};
    if(isLeapYear(d.year))
        printf("%d is a leap year\n", d.year);
    else
        printf("%d is not a leap year\n", d.year);
    return 0;
}
```
## 7.Define a structure to represent a complex number with real and imaginary parts (both floats). Write a function to add two complex numbers represented by structures.
```c
#include <stdio.h>
struct Complex {
    float real, imag;
};
struct Complex add(struct Complex a, struct Complex b) {
    struct Complex result;
    result.real = a.real + b.real;
    result.imag = a.imag + b.imag;
    return result;
}
int main() {
    struct Complex c1 = {2.5, 3.5}, c2 = {1.5, 4.5}, sum;
    sum = add(c1, c2);
    printf("Sum = %.2f + %.2fi\n", sum.real, sum.imag);
    return 0;
}
```
## 8.Implement a linked list using structures. Each node in the list should hold an integer value and a pointer to the next node.
```c
#include <stdio.h>
#include <stdlib.h>
struct Node {
    int data;
    struct Node* next;
};
void printList(struct Node* head) {
    while(head) {
        printf("%d -> ", head->data);
        head = head->next;
    }
    printf("NULL\n");
}
int main() {
    struct Node *head=NULL, *second=NULL, *third=NULL;
    head = (struct Node*)malloc(sizeof(struct Node));
    second = (struct Node*)malloc(sizeof(struct Node));
    third = (struct Node*)malloc(sizeof(struct Node));
    head->data=10; head->next=second;
    second->data=20; second->next=third;
    third->data=30; third->next=NULL;

    printList(head);
    return 0;
}
```
## 9.Define a self-referential structure to represent a binary tree node. Each node should have data (integer) and pointers to left and right child nodes.
```c
#include <stdio.h>
#include <stdlib.h>
struct Node {
    int data;
    struct Node* left;
    struct Node* right;
};
int main() {
    struct Node* root = (struct Node*)malloc(sizeof(struct Node));
    root->data = 10;
    root->left = root->right = NULL;
    printf("Root node data: %d\n", root->data);
    return 0;
}
```
## 10.Read student data from file into array of structures
```c
#include <stdio.h>
#include <stdlib.h>

struct Student {
    char name[50];
    int roll;
    float marks;
};

int main() {
    FILE *fp = fopen("students.txt", "r");
    if (!fp) {
        printf("Error opening file!\n");
        return 1;
    }

    struct Student students[100];
    int count = 0;

    while (fscanf(fp, "%s %d %f", students[count].name, 
                  &students[count].roll, 
                  &students[count].marks) == 3) {
        count++;
    }
    fclose(fp);

    printf("Student Data:\n");
    for (int i = 0; i < count; i++) {
        printf("%s %d %.2f\n", students[i].name, students[i].roll, students[i].marks);
    }
    return 0;
}
```
## 11.Check if date is valid
```c
#include <stdio.h>

struct Date {
    int day, month, year;
};

int isLeapYear(int year) {
    return (year % 400 == 0) || (year % 100 != 0 && year % 4 == 0);
}

int isValidDate(struct Date d) {
    if (d.year < 1 || d.month < 1 || d.month > 12 || d.day < 1)
        return 0;

    int daysInMonth[] = {0,31,28,31,30,31,30,31,31,30,31,30,31};

    if (isLeapYear(d.year)) daysInMonth[2] = 29;

    return d.day <= daysInMonth[d.month];
}

int main() {
    struct Date d = {29, 2, 2024};
    if (isValidDate(d))
        printf("Valid date\n");
    else
        printf("Invalid date\n");
    return 0;
}
```
