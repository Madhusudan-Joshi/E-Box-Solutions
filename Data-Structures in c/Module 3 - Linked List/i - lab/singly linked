#include<stdio.h>
#include<stdlib.h>

struct node
{
    char usn[25],name[25],branch[25];
    int sem;
    char phone[25];
    struct node *link;
};
typedef struct node * NODE;

NODE start = NULL;
int count=0;


NODE create()
{
    NODE snode;
    snode = (NODE)malloc(sizeof(struct node));

    if(snode == NULL)
    {
        printf("\nMemory is not available");
        exit(1);
    }
    printf("Enter USN\n");
    scanf("%s",snode->usn);
    printf("Enter Name\n");
    scanf("%s",snode->name);
    printf("Enter Branch\n");
    scanf("%s",snode->branch);
    printf("Enter Phone number\n");
    scanf("%s",snode->phone);
    printf("Enter Sem\n");
    scanf("%d",&snode->sem);
    
    snode->link=NULL;
    count++;
    return snode;
}

NODE create2()
{
    NODE snode;
    snode = (NODE)malloc(sizeof(struct node));

    if(snode == NULL)
    {
        printf("\nMemory is not available");
        exit(1);
    }
    printf("Enter USN");
    scanf("%s",snode->usn);
    printf("Enter Name");
    scanf("%s",snode->name);
    printf("Enter Branch");
    scanf("%s",snode->branch);
    printf("Enter Sem");
    scanf("%d",&snode->sem);
    printf("Enter Ph.No\n");
    scanf("%s",snode->phone);
    
    snode->link=NULL;
    count++;
    return snode;
}

NODE insertfront2()
{
    NODE temp;
    temp = create2();
    if(start == NULL)
    {
           return temp;
    }

    temp->link = start;
    return temp;
}

NODE insertfront()
{
    NODE temp;
    temp = create();
    if(start == NULL)
    {
           return temp;
    }

    temp->link = start;
    return temp;
}

NODE deletefront()
{
    NODE temp;
    if(start == NULL)
    {
        printf("\nLinked list is empty");
        return NULL;
    }

    if(start->link == NULL)
    {
            printf("\nFront(first) node is deleted");
            count--;
            free(start);
            return NULL;
    }
    temp = start;
    start = start->link;
  printf("\nFront(first) node is deleted");
    count--;
    free(temp);
    return start;
}


NODE insertend2()
{
    NODE cur,temp;
    temp = create2();

    if(start == NULL)
    {
      return temp;
    }
    cur = start;
    while(cur->link !=NULL)
    {
         cur = cur->link;
    }
    cur->link = temp;
    return start;
}




NODE insertend()
{
    NODE cur,temp;
    temp = create();

    if(start == NULL)
    {
      return temp;
    }
    cur = start;
    while(cur->link !=NULL)
    {
         cur = cur->link;
    }
    cur->link = temp;
    return start;
}



NODE deleteend()
{
     NODE cur,prev;
     if(start == NULL)
     {
        printf("\nLinked List is empty");
        return NULL;
     }

     if(start->link == NULL)
     {
        printf("\nLast (end) node is deleted");
        free(start);
        count--;
        return NULL;
     }

     prev = NULL;
     cur = start;
     while(cur->link!=NULL)
     {
         prev = cur;
         cur = cur->link;
     }

    printf("\nLast (end) node is deleted");
      free(cur);
      prev->link = NULL;
      count--;
      return start;
}



void display()
{
    NODE cur;
    int num=1;


    if(start == NULL)
    {

        printf("\nNo Contents to display in SLL \n");
        return;
    }
    printf("\nSTUDENT Details\n");
    cur = start;
    printf("USN NAME BRANCH SEM Ph.NO.\n");
    while(cur!=0)
    {
       printf("\n%s %s %s %d ",cur->usn, cur->name,cur->branch, cur->sem);
       printf("%s",cur->phone);
       cur = cur->link;
       num++;
    }
    printf("\nThe no.of nodes in list is %d \n",count);
}

void stackdemo()
{
   int ch;
   while(1)
   {
     printf("\nSSL used as Stack");
     printf("\n1.Insert at Front(PUSH)\n2.Delete from Front(POP)\n3.Exit\n");
     printf("\nEnter your choice:\n");
     scanf("%d",&ch);

     switch(ch)
     {
        case 1: start = insertfront2();
                display();
                break;
        case 2: start = deletefront();
                display();
                break;
        case 3: printf("exit");
               return;
               break;
       default : return;
     }
   }
   return;
}

void INSERT()
{
    int ch;
    while(1)
    {
        printf("\n1.Insert at Front(First)");
        printf("\n2.Insert at End(Rear/Last)");
        printf("\n3.Exit\n");
        printf("\nEnter your choice");
        scanf("%d",&ch);
        
        switch(ch)
        {
            case 1: start = insertfront2();
                    display();
                    break;
            case 2: start = insertend2();
                    display();
                    break;
            case 3: printf("exit"); return;
                    break;
            default: return;
        }
    }
}

void DELETE()
{
    int ch;
    while(1)
    {
        printf("\n1.Delete from Front(First)");
        printf("\n2.Delete from End(Rear/last)");
        printf("\n3.Exit\n");
        printf("\nEnter your choice");
        scanf("%d",&ch);
        
        switch(ch)
        {
            case 1: start = deletefront();
                    display();
                    break;
            case 2: start = deleteend();
                    display();
                    break;
            case 3: printf("Exit"); return;
                    break;
            default: return;
        }
    }
}



void queuedemo()
{
    int ch;
    while(1)
    {
        printf("\nSSL used as Queue");
        printf("\n1.Insert at Rear(INSERT)");
        printf("\n2.Delete from Front(DELETE)");
        printf("\n3.Exit\n");
        printf("\nEnter your choice:");
        scanf("%d",&ch);
        
        switch(ch)
        {
            case 1: start = insertfront2();
                    display();
                    break;
            case 2: start = deletefront();
                    display();
                    break;
            case 3: printf("Exit"); return;
                    break;
            default: return;
        }
    }
}

int main()
{
    int ch,i,n;
    printf("\nStudendts Details\n");
    while(1)
    {
        
        printf("\n1 Create");
        printf("\n2 Display");
        printf("\n3 Insert");
        printf("\n4 Delete");
        printf("\n5 Stack");
        printf("\n6 Queue");
        printf("\n7 Exit");
        printf("\nEnter your choice");
        scanf("%d",&ch);

        switch(ch)
        {
        case 1 : printf("\nHow many student data you want to create\n");
                 scanf("%d",&n);
                 for(i=1;i<=n;i++)
                    start = insertend();
                 break;

        case 2: display();
                break;

        case 3: INSERT();
                break;

        case 4: DELETE(); 
                break;

        case 5: stackdemo();
                break;

        case 6: queuedemo();
                break;
        case 7: printf("exit");
                exit(0);
                break;

        default: printf("\nPlease enter the valid choice");

        }
    }
}
