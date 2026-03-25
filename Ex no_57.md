

# EX 57 C function to perfom push,pop and peek functions in Stack using Linked List.( store char data in stack)
## DATE:
## AIM:
To write a C function to perfom push,pop and peek functions in Stack using Linked List.

## Algorithm


1. **Start**  
2. Define a structure `Node` with two fields:  
   - `data` (float type)  
   - `next` (pointer to the next node)  
3. Initialize `top` as `NULL` (empty stack).  
4. **Push Operation:**  
   - Create a new node.  
   - Assign the float value to `data`.  
   - Set `next` to `top`.  
   - Update `top` to point to the new node.  
5. **Pop Operation:**  
   - Check if `top` is `NULL` (stack is empty).  
   - If not, store `top->data`.  
   - Update `top` to `top->next`.  
   - Free the popped node’s memory.  
6. **Peek Operation:**  
   - Check if `top` is `NULL`.  
   - If not, display `top->data`.  
7. **End**  



## Program:
```
struct Node   
{  
char data;  
struct Node *next;  
}*head,*t;
void push(int data)  
{  
    struct Node *n=(struct Node *)malloc(sizeof(struct Node));
    n->data=data;
    n->next=0;
    if(head==NULL)
    {
        head=n;
    }
    else
    {
        n->next=head;
        head=n;
    }
}  
void pop()  
{  
    if(head==NULL)
    {
        printf(" ");
    }
    else
    {
        head=head->next;
    }
}  
void display()  
{  
    if(head==NULL)
    {
        printf(" ");
    }
    else
    {
        printf("stack:");
        t=head;
        while(t!=0)
        {
            printf("%c ",t->data);
            t=t->next;
        }
        printf("\n");
    }
}  
void peek()
{
    printf("stack top:%c\n",head->data);
}
```

## Output:


![image](https://github.com/user-attachments/assets/76a14460-31cd-40b9-92f1-ee0f025b5ec7)

## Result:
Thus the program was executed and the output was verified successfully.
