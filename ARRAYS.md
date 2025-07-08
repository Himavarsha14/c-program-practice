## 1.C Program to reverse an array using temporary array
```c
#include <stdio.h>
#include <stdlib.h>
void reverseArray(int arr[], int n) {
    int temp[n];
    for(int i = 0; i < n; i++)
        temp[i] = arr[n - i - 1];
    for(int i = 0; i < n; i++)
        arr[i] = temp[i];
}
int main() {
    int arr[] = { 1, 4, 3, 2, 6, 5 };
    int n = sizeof(arr) / sizeof(arr[0]);
    reverseArray(arr, n);
    for(int i = 0; i < n; i++) 
        printf("%d ", arr[i]);
    return 0;
}
```

## 2.C program to find sum of all elements in an array
```c
#include<stdio.h>
int main()
{
        int n;
        printf("Enter the size of array:\n");
        scanf("%d",&n);
        int arr[n];
        printf("Enter elements of an array:\n");
        for(int i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        int *ptr;
        ptr=arr;
        int sum=0;
        for(int i=0;i<n;i++)
        {
                sum=sum+*(ptr+i);
        }
        printf("The sum of elements in the array is:%d\n",sum);
        return 0;
}
```


## 3.C Program to copy the elements of one array to another array
```c
#include<stdio.h>
int main()
{
        int n;
        printf("Enter size of the array:\n");
        scanf("%d",&n);
        int arr1[n],arr2[n];
    printf("Enter elements of array:\n");
        for(int i=0;i<n;i++)
        {
                scanf("%d",&arr1[i]);
        }
        int *ptr1,*ptr2;
        ptr1=arr1;
        ptr2=arr2;
        for(int i=0;i<n;i++)
        {
                *(ptr2+i)=*(ptr1+i);
                printf("%d ",*(ptr2+i));
        }
        return 0;
}
```
## 4.Program to count total number of duplicate elements in an array
```c
#include<stdio.h>
int main()
{
        int n;
        printf("Enter the size of the array:\n");
        scanf("%d",&n);
        int arr[n];
        printf("Enter the elements of the array:\n");
        for(int i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        int count=0;
        for(int i=0;i<n;i++)
        {
                for(int j=i+1;j<n;j++)
                {
                        if(arr[i]==arr[j])
                        {
                                count++;
                                break;
                        }
                }

        }
        if(count>1)
        {
                printf("The total number of duplicates in the array are:%d\n",count);
        }
        return 0;
}
```

## 5.Program to print all unique elements
```c
#include<stdio.h>
int main()
{
        int n;
        printf("Enter the size of the array:\n");
        scanf("%d",&n);
        int arr[n];
        printf("Enter the elements of array:\n");
        int i,j;
        for(i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        printf("The unique elements are:\n");
        for(i=0;i<n;i++)
        {
                int count=0;
                for(j=0;j<n;j++)
                {
                        if(arr[i]==arr[j])
                        {
                                count++;
                        }
                }
                if(count==1)
                {
                        printf("%d ",arr[i]);           }

        }
        printf("\n");

        return 0;
}
```
## 6.Program to find the largest and smallest element in an array
```c
#include<stdio.h>
int main()
{
        int n;
        printf("Enter the size of the array:\n");
        scanf("%d",&n);
        int arr[n];
        printf("Enter the elements of an array:\n");
        for(int i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        int *ptr=arr;
        int largest_element=*ptr;
        int smallest_element=*ptr;
        for(int i=0;i<n;i++)
        {
                if(*(ptr+i)>largest_element)

                        largest_element=*(ptr+i);
                if(*(ptr+i)<smallest_element)
                        smallest_element=*(ptr+i);
        }
        printf("The largest element in the given array is:%d\n",largest_element);
        printf("The smallest element in the given array is:%d\n",smallest_element);
        return 0;
}
```
## 7.Program to merge two arrays into a third array
```c
#include<stdio.h>
int main()
{
        int n1,n2;
        printf("Enter the size of array1 and array 2:\n");
        scanf("%d %d",&n1,&n2);
        int arr1[n1],arr2[n2];
        printf("Enter the elements of first array:\n");
        for(int i=0;i<n1;i++)
        {
                scanf("%d",&arr1[i]);
        }
        printf("Enter the elements of second array:\n");
        for(int i=0;i<n2;i++)
        {
                scanf("%d",&arr2[i]);
        }
        int mergedarr[n1+n2];
        for(int i=0;i<n1;i++)
        {
                mergedarr[i]=arr1[i];
        }
        for(int i=0;i<n2;i++)
        {
                mergedarr[n1+i]=arr2[i];
        }
        printf("Merged array\n");
        for(int i=0;i<n1+n2;i++)
        {
                printf("%d ",mergedarr[i]);
        }
        return 0;
}
```
## Program to insert an element at a given positi

