#include<stdio.h>
#include<stdlib.h>
void create();
void display();
void insert_beg();
void insert_end();
void delete_beg();
void delete_end();
void delete_node();
void avearge();
void insert_sorted();
void reverse();
 
struct node
{
 int info;
 struct node*link;
};
struct node*start=NULL;

void create()
{
    struct node*temp,*ptr;
    temp=(struct node*)malloc(sizeof(struct node));

     if(temp==NULL)
     {
       printf("out of memory space:");
       exit(0);
     }
     printf("Enter the data value for the node:");
     scanf("%d",temp->info);
     temp->link=NULL;
     if(start==NULL)
     {
       start=temp;
     }
     else
     {
        ptr=start; 
         while(ptr->link!=NULL)
        {
          ptr=ptr->link;
        }
        ptr->link=temp;
  }
}
void display()
{
  struct node*ptr;
    if(start==NULL)
    {
      ptr=start;
      printf("the list elements are:");
         while(ptr!=NULL)
        {
	     printf("%d",ptr->info);
          ptr=ptr->link;
        }
    }
}
void insert_beg()
{
  int data;
   struct node*temp,*head;
   temp=malloc(sizeof(struct node));
 
   printf("\n Enter number to be inserted:");
   scanf("%d",data);
 
    temp->link=0;
    temp->info=data;
    head=start
       while(head->link!=NULL)
       {
         head=head->link;
       }
      head->link=temp;
}
void delete_end()
{
   struct node*temp,*prev_node;
    if(start==NULL)
      printf("\nlist is empty\n");
    else
    {
       temp=start;
        while(temp->link!=0)
        {
           prev_node=temp;
           temp=temp->link;  
    }
    free(temp);
    prev_node->link=0;
 }
}
void delete_node()
{
  struct node *temp,*position
  int i=1,pos;
  
  if(start==NULL)
       printf("\nlist is empty\n");
  else    
  {
       printf("\nEnter index:");
       scanf("%d",pos);
       position=malloc(sizeof(struct node));
       temp=start;
       while(i<pos-1)
       {
         temp=temp->link;
         i++;
       } 
       position=temp->link;
       temp->link=position->link;
       free(position);
   }
}
void average()
{
  struct node*ptr=start;
  int sum=0,count=0,avg;
  while(ptr1=NULL)
  {
    sum=sum+ptr->info;
    count++;
    ptr=ptr->link;
  } 
  avg=sum/count;
  printf("average is %d",avg);
}
void insert_sorted()
{
   struct node*current=start;
   struct node*index=NULL;
   int temp;
   
   if(start==NULL)
   {
     return;
   }
   else
   {
     while(current!=NULL)
     {
       index=current->link;
       
       while(index!=NULL)
       {
         if(current->info>index->info)
         {
           temp=current->info
           current->info=index->info;
           index->info=temp;
         }
         index=index->link;
        }
        current=current->link;
      }
    }
}
void reverse()
{
  struct node*t1,*t2,*temp;
  t1=t2=NULL;
  
  if(start==NULL)
   {
     printf("list is empty");
     
  else
  {
    while(start!=NULL)
    {
      t2=start->link;
      start->link=t1;
      t1=start
      start=t2;
    }
    start=t1;
    
    temp

   
    
   
  
   
  
      
