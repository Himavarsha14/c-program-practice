## 1.Insert at end
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead=NULL;
void insert_end(int d)
{
        struct node *pnew;
        pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=d;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
                return;
        }
        struct node *ptrav;
        ptrav=phead;
        while(ptrav->next!=NULL)
        {
            ptrav=ptrav->next;
        }
        ptrav->next=pnew;
}
void display()
{
        struct node *ptrav;
        ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
}
int main()
{
        int i,data,n;
        printf("Enter number of nodes:\n");
        scanf("%d",&n);
        for(i=0;i<n;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_end(data);
        }
        printf("The elements in the list are:\n");
        display();
        return 0;
}
```
## 2.Delete at end
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead=NULL;
void insert_end(int d)
{
        struct node *pnew;
        pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=d;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
                return;
        }
        struct node *ptrav;
        ptrav=phead;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pnew;
}
void delete_end()
{
        struct node *ptrav,*prevtrav;
        ptrav=phead;
        prevtrav=NULL;
        while(ptrav->next!=NULL)
        {
                prevtrav=ptrav;
                ptrav=ptrav->next;
        }
        prevtrav->next=NULL;
        free(ptrav);
}
void display()
{
        struct node *ptrav;
        ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
}
int main()
{
        int i,data,n;
        printf("Enter number of nodes:\n");
        scanf("%d",&n);
        for(i=0;i<n;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_end(data);
        }
        printf("List before deleting last node\n");
        display();
        printf("\n");
        printf("List after deleting last node\n");
        delete_end();
        display();
}
```
## 3.Insert at Head/Beginning
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead=NULL;
void insert_head(int d)
{
        struct node *pnew;
        pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=d;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
        }
        else
        {
                pnew->next=phead;
                phead=pnew;
        }
}
void display()
{
        struct node *ptrav;
        ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
}
int main()
{
        int nodes,data,i;
        printf("Enter number of nodes:\n");
        scanf("%d",&nodes);
        for(i=0;i<nodes;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_head(data);
        }
        printf("The elements in the list are:\n");
        display();
        return 0;
}
```
## 4.Delete at Head/Beginning
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead=NULL;
void insert_head(int d)
{
        struct node *pnew;
        pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=d;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
        }
        else
        {
                pnew->next=phead;
                phead=pnew;
        }
}
void delete_at_begining()
{
        if(phead==NULL)
        {
                printf("List is empty\n");
                return;
        }
        struct node *temp;
        temp=phead;
        phead=phead->next;
        free(temp);
}
void display()
{
        struct node *ptrav;
        ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
        printf("\n");
}
int main()
{
        int nodes,data,i;
        printf("Enter number of nodes:\n");
        scanf("%d",&nodes);
        for(i=0;i<nodes;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_head(data);
        }
        printf("The elements in the list are:\n");
        display();
        delete_at_begining();
        printf("The elements after deleting node at begin:\n");
        display();
        return 0;
}

```
## 5.Insertion before a node
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead=NULL;
void insert_end(int d)
{
        struct node *pnew;
        pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=d;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
        }
        else
        {
                struct node *ptrav;
                ptrav=phead;
                while(ptrav->next!=NULL)
                {
                        ptrav=ptrav->next;
                }
                ptrav->next=pnew;
        }
}
void display()
{
        struct node *ptrav;
        ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
}
void insert_before(int target,int newdata)
{
        struct node *newnode;
        newnode=(struct node*)malloc(sizeof(struct node));
        if(newnode==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        newnode->data=newdata;
        newnode->next=NULL;
        if(phead==NULL)
        {
                printf("List is empty\n");
                return;
        }
        if(phead->data==target)
        {
                newnode->next=phead;
                phead=newnode;
        }
        else
        {
                struct node *ptrav,*prev;
                ptrav=phead;
                prev=NULL;
                while(ptrav!=NULL && ptrav->data!=target)
                {
                        prev=ptrav;
                        ptrav=ptrav->next;
                }
                if(ptrav==NULL)
                {
                        printf("Target not found\n");
                        free(newnode);
                        return;
                }
                prev->next = newnode;
                newnode->next = ptrav;
        }
}
int main()
{
        int nodes,data,target,newdata,i;
        printf("Enter number of nodes:\n");
        scanf("%d",&nodes);
        for(i=0;i<nodes;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_end(data);
        }
        printf("Enter target and newdata:\n");
        scanf("%d %d",&target,&newdata);
        insert_before(target,newdata);
        display();
        return 0;
}
```
## 6.Insertion in the middle of the linked list
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
                struct node *next;
        };
        struct node *phead;
        void insert_end(int data)
        {
                struct node *pnew;
                pnew=(struct node*)malloc(sizeof(struct node));
                if(pnew==NULL)
                {
                        printf("Malloc error\n");
                        return;
                }
                pnew->data=data;
                pnew->next=NULL;
                if(phead==NULL)
                {
                        phead=pnew;
                        return ;
                }
                struct node *ptrav=phead;
                while(ptrav->next!=NULL)
                {
                        ptrav=ptrav->next;
                }
                ptrav->next=pnew;
        }
void insert_middle(int mdata)
{
        struct node *newnode;
        newnode=(struct node*)malloc(sizeof(struct node));
        if(newnode==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        newnode->data=mdata;
        newnode->next=NULL;
        struct node *fast,*slow;
        fast=phead;
        slow=phead;
        struct node *ptr;
        while(fast!=NULL && fast->next!=NULL)
        {
                ptr=slow;
                slow=slow->next;
                fast=fast->next->next;
        }
        newnode->next=ptr->next;
        ptr->next=newnode;
}
void display()
{
        struct node *ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d->",ptrav->data);
                ptrav=ptrav->next;
        }
}
int main()
{
        int nodes,data,mdata,i;
        printf("Enter number of nodes:\n");
        scanf("%d",&nodes);
        for(i=0;i<nodes;i++)
        {
                printf("Data for nodes %d:\n",i+1);
                scanf("%d",&data);
                insert_end(data);
        }
        display();
        printf("\n");
        printf("Enter data for middle node:\n");
        scanf("%d",&mdata);
        insert_middle(mdata);
        display();
        return 0;
}
```
## 7.Deleting middle node of a linked list
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead;
void insert_end(int data)
{
        struct node *pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=data;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
                return;
        }
        struct node *ptrav=phead;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pnew;
}
void delete_middle()
{
        struct node *slow,*fast,*p;
        slow=phead;
        fast=phead;
        while(fast!=NULL && fast->next!=NULL)
        {
                p=slow;
                slow=slow->next;
                fast=fast->next->next;
        }
        p->next=slow->next;
        free(slow);
}
void display()
{
        struct node *ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d->",ptrav->data);
                ptrav=ptrav->next;
        }
}
int main()
{
        int nodes,data,i;
        printf("Enter number of nodes:\n");
        scanf("%d",&nodes);
        for(i=0;i<nodes;i++)
        {
                printf("Data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_end(data);
        }
        display();
        printf("\n");
        printf("Deleting after middle node:\n");
        delete_middle();
        display();
        printf("\n");
        return 0;
}
```
## 8.Creation of loop in linked list
```c
include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead;
void insert_end(int data)
{
        struct node *pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=data;
        pnew->next=NULL;
        struct node *ptrav=phead;
        if(phead==NULL)
        {
                phead=pnew;
                return;
        }
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pnew;
}
void create_loop()
{
        struct node *ptrav=phead;
        struct node *pp=phead->next;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pp;
}
void display()
{
        struct node *ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
}
int main()
{
        int n;
        printf("Number of nodes:\n");
        scanf("%d",&n);
        int data;
        for(int i=0;i<n;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_end(data);
        }
        printf("Linked list before loop creation:\n");
        display();
        create_loop();
        //display();       //calling display again to check whether loop is create or not
        return 0;
}

```
## 9.Detection of loop in linked list
```c
include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead;
void insert_end(int data)
{
        struct node *pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=data;
        pnew->next=NULL;
        struct node *ptrav=phead;
        if(phead==NULL)
        {
                phead=pnew;
                return;
        }
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pnew;
}
void create_loop()
{
        struct node *ptrav=phead;
        struct node *pp=phead->next;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pp;
}
int detect_loop()
{
        struct node *slow=phead;
        struct node *fast=phead;
        while(slow && fast && fast->next)
        {
                slow=slow->next;
                fast=fast->next->next;
                if(slow==fast)
                {
                        return 1;
                }
        }
        return 0;
}
void display()
{
        struct node *ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
}
int main()
{
        int n;
        printf("Number of nodes:\n");
        scanf("%d",&n);
        int data;
        for(int i=0;i<n;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_end(data);
        }
        printf("Linked list before loop creation:\n");
        display();
        create_loop();
        if(detect_loop())
        {
                printf("\nLoop detected\n");
        }
        else
        {
                printf("Loop not detected\n");
        }
        //display();       //calling display again to check whether loop is create or not
        return 0;
}
```
## 10.Reversing a Linked list
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead=NULL;
void insert_begin(int data)
{
        struct node *pnew=(struct node *)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=data;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
        }
        else
        {
                pnew->next=phead;
                phead=pnew;
        }
}
void display()
{
        struct node *ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
}
void reverse()
{
        struct node *curr=phead;
        struct node *next=NULL;
        struct node *prev=NULL;
        while(curr!=NULL)
        {
                next=curr->next;
                curr->next=prev;
                prev=curr;
                curr=next;
        }
        phead=prev;
}
int main()
{
        int nodes,data,i;
        printf("NUmber of nodes:\n");
        scanf("%d",&nodes);
        for(i=0;i<nodes;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_begin(data);
        }
        printf("Linked list before reversal:\n");
        display();
        printf("\nLinked list after reversal:\n");
        reverse();
        display();

}
```
## 11.Program to merge two lists
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead=NULL;
struct node *phead1=NULL;
void list1(int data1)
{
        struct node *pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=data1;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
                return;
        }
        struct node *ptrav=phead;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pnew;
}
void list2(int data2)
{
        struct node *pnew1=(struct node*)malloc(sizeof(struct node));
        if(pnew1==NULL)
        {
                printf("Malloc erroe\n");
        }
        pnew1->data=data2;
        pnew1->next=NULL;
        if(phead1==NULL)
        {
                phead1=pnew1;
                return;
        }
        struct node *ptrav=phead1;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pnew1;
}
void merge()
{
        struct node *ptrav=phead;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=phead1;
}
void display()
{
        struct node *ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
        printf("\n");
}
void display2()
{
        struct node *ptrav=phead1;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
        printf("\n");
}

int main()
{
        int n1,n2,i,data1,data2;
        printf("Number of nodes for list1:\n");
        scanf("%d",&n1);
        printf("Number of nodes for list2:\n");
        scanf("%d",&n2);
        for(i=0;i<n1;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data1);
                list1(data1);
        }
        printf("List 1:\n");
        display();
        printf("\n");
        for(i=0;i<n2;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data2);
                list2(data2);
        }
        printf("List 2:\n");
        display2();
        printf("Merged list:\n");
        merge();
        display();
        return 0;
}
```
## 12.Rotate linked list by one position left
```c
#include<stdio.h>
#include<stdlib.h>
struct node
{
        int data;
        struct node *next;
};
struct node *phead=NULL;
void insert_end(int data)
{
        struct node *pnew=(struct node*)malloc(sizeof(struct node));
        if(pnew==NULL)
        {
                printf("Malloc error\n");
                return;
        }
        pnew->data=data;
        pnew->next=NULL;
        if(phead==NULL)
        {
                phead=pnew;
                return;
        }
        struct node *ptrav=phead;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=pnew;
}
void rotate_left()
{
        struct node *ptemp,*ptrav;
        ptrav=phead;
        ptemp=phead;
        phead=phead->next;
        while(ptrav->next!=NULL)
        {
                ptrav=ptrav->next;
        }
        ptrav->next=ptemp;
        ptemp->next=NULL;

}
void display()
{
        struct node *ptrav=phead;
        while(ptrav!=NULL)
        {
                printf("%d ",ptrav->data);
                ptrav=ptrav->next;
        }
        printf("\n");
}
int main()
{
        int nodes,data,i;
        printf("Number of nodes:\n");
        scanf("%d",&nodes);
        for(i=0;i<nodes;i++)
        {
                printf("Enter data for node %d:\n",i+1);
                scanf("%d",&data);
                insert_end(data);
        }
        printf("List before rotating:\n");
        display();
        printf("List after rotating left by one position:\n");
        rotate_left();
        display();
        return 0;
}
```
