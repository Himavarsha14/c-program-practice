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
## 7.Delete at Head/Beginning
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
