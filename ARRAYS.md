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
## 8.Program to insert an element at a given position
```c
#include<stdio.h>
int main()
{
        int n,element,pos;
        printf("Enter the size of the array:\n");
        scanf("%d",&n);
        int arr[n];
        printf("Enter elements of arrays:\n");
        for(int i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        printf("Enter the element to insert:\n");
        scanf("%d",&element);
        printf("Enter the position to insert:\n");
        scanf("%d",&pos);
        if(pos<0||pos>n)
        {
                printf("Invalid position!\n");
                return 1;
        }
        for(int i=n;i>pos;i--)
        {
                arr[i]=arr[i-1];
        }
        arr[pos]=element;
        n++;
        printf("Array after insertion:\n");
        for(int i=0;i<n;i++)
        {
                printf("%d ",arr[i]);
        }
        printf("\n");
        return 0;
}
```
## 9.Program to find Second largest element in an array
```c
#include<stdio.h>
#include<limits.h>
int main()
{
        int n,i;
        printf("Enter the size of array:\n");
        scanf("%d",&n);
        int arr[n];
        printf("Enter the elements of array:\n");
        for(int i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        int largest=INT_MIN;
        int sec_lar=INT_MIN;
        for(i=0;i<n;i++)
        {
                if(arr[i]>largest)
                {
                        sec_lar=largest;
                        largest=arr[i];
                }
                else if(arr[i]>sec_lar && arr[i]!=largest)
                {
                        sec_lar=arr[i];
                }
        }
printf("The second largest element in the array is:%d",sec_lar);
return 0;
}
```
## 10.Program to find missing element in an array
```c
#include<stdio.h>
int main()
{
        int n,i;
        printf("Enter the size of the array:\n");
        scanf("%d",&n);
        int arr[n];
        printf("Enter the elements of the array:\n");
        for(i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        int expected_sum=n*(n+1)/2;
        int actual_sum=0;
        for(int i=0;i<n-1;i++)
        {
                actual_sum+=arr[i];
        }
        int missing_number=expected_sum-actual_sum;
        printf("The missing element is:%d",missing_number);
        return 0;
}

```
## 11.Program to find Duplicate elements
```c
include<stdio.h>
int main()
{
        int n;
        printf("Enter the size of array:\n");
        scanf("%d",&n);
        int arr[n];
        printf("Enter the elements of the array:\n");
        for(int i=0;i<n;i++)
        {
                scanf("%d",&arr[i]);
        }
        printf("The duplicates:\n");
        for(int i=0;i<n;i++)
        {
                int count=0;
                for(int j=i+1;j<n;j++)
                {
                        if(arr[i]==arr[j])
                        {
                                count++;
                                break;
                        }
                }
        int visited=0;
        for(int k=0;k<i;k++)
        {
                if(arr[k]==arr[i])
                {
                        visited=1;
                        break;
                }
        }
        if(count>0&&!visited)
        {
                printf("%d\n",arr[i]);
        }
}
        return 0;
}
```
## 12.Program to rotate array Left by 1
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
        printf("Enter original array:\n");
        for(int i=0;i<n;i++)
        {
                printf("%d ",arr[i]);
        }
        printf("\n");
        int temp=arr[0];
        for(int i=0;i<n-1;i++)
        {
                arr[i]=arr[i+1];
        }
        arr[n-1]=temp;
        printf("Rotated array:\n");
        for(int i=0;i<n;i++)
        {
                printf("%d ",arr[i]);
        }
        return 0;
}
```
## 13.Program to rotate array Right by 1
```c
#include<stdio.h>
int main()
{
    int n;
    printf("Enter the size of the array:\n");
    scanf("%d",&n);
    int arr[n];
    printf("Enter the elements of array:\n");
    for(int i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    int temp=arr[n-1];
    for(int i=n-1;i>0;i--)
    {
        arr[i]=arr[i-1];
    }
    arr[0]=temp;
    printf("Array after rotating right by one position:\n");
    for(int i=0;i<n;i++)
    {
        printf("%d ",arr[i]);
    }
    return 0;
}
```
## 14. C program to left rotate an array by k positions using the shifting method
```c
#include <stdio.h>

int main()
{
    int n, k;
    printf("Enter the size of the array:\n");
    scanf("%d", &n);

    int arr[n];
    printf("Enter %d elements of the array:\n", n);
    for(int i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }

    printf("Enter number of positions to rotate left (k):\n");
    scanf("%d", &k);
    int temp;
    for(int i = 0; i < k; i++)
    {
        temp = arr[0];
        for(int j = 0; j < n - 1; j++)
        {
            arr[j] = arr[j + 1];
        }
        arr[n - 1] = temp;
    }

    printf("Array after left rotating by %d positions:\n", k);
    for(int i = 0; i < n; i++)
    {
        printf("%d ", arr[i]);
    }

    return 0;
}
```
## 15. C program to right rotate an array by k positions using the shifting method
```c
#include<stdio.h>
int main()
{
    int n;
    printf("Enter size of the array:\n");
    scanf("%d",&n);
    int arr[n];
    printf("Enter the elements of array:\n");
    for(int i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    int k;
    printf("Number of positions:\n");
    scanf("%d",&k);
    int temp;
    for(int i=0;i<k;i++)
    {
        temp=arr[n-1];
        for(int j=n-1;j>0;j--)
        {
            arr[j]=arr[j-1];
        }
        arr[0]=temp;
    }
    printf("Array after rotating %d positions\n",k);
     for(int i=0;i<n;i++)
        {
            printf("%d ",arr[i]);
            
        }
    
    return 0;
}
```
## 16. Program to find the maximum sum of any contiguous subarray of size k
```c
#include <stdio.h>
int main() {
    int n;
    printf("Enter size of the array:\n");
    scanf("%d", &n);
    int arr[n];
    printf("Enter the elements of array:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    int k;
    printf("Enter window size k:\n");
    scanf("%d", &k);

    int window_sum = 0;
    for (int i = 0; i < k; i++) {
        window_sum += arr[i];
    }

    int max_sum = window_sum;

    for (int i = k; i < n; i++) {
        window_sum = window_sum - arr[i - k] + arr[i];
        if (window_sum > max_sum) {
            max_sum = window_sum;
        }
    }

    printf("Maximum sum of subarray of size %d is: %d\n", k, max_sum);
    return 0;
}
```
## 17.Count Subarrays with Sum ≤ K
```c
#include <stdio.h>

int main() {
    int n;
    printf("Enter the size of the array:\n");
    scanf("%d", &n);

    int arr[n];
    printf("Enter elements of the array:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    int k;
    printf("Enter the maximum allowed subarray sum (k):\n");
    scanf("%d", &k);

    int count = 0;

    // Loop through all subarrays
    for (int i = 0; i < n; i++) {
        int sum = 0;
        for (int j = i; j < n; j++) {
            sum += arr[j];
            if (sum <= k) {
                count++;
            } else {
                break; // No point in checking longer subarray if sum already > k
            }
        }
    }

    printf("Number of subarrays with sum less than or equal to %d is: %d\n", k, count);
    return 0;
}
```


