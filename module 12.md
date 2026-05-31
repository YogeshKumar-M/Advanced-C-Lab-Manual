# EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display stack elements using linked list.

## Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
## Program:
```
#include <stdio.h>
#include <stdlib.h>
struct Node {
int data;
struct Node *next;
};
struct Node *head = NULL;
void display() {
struct Node *p = head;
while (p != NULL) {
printf("%d ", p->data);
p = p->next;
}
printf("\n");
}
void insert(int value) {
struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
newNode->data = value;
newNode->next = NULL;
if (head == NULL)
head = newNode;
else {
struct Node *temp = head;
while (temp->next != NULL)
temp = temp->next;
temp->next = newNode;
}
}
int main() {
insert(10);
insert(20);
insert(30);
 printf("Linked List elements are: ");
display();
return 0;
}
```
## Output:
<img width="749" height="593" alt="517984688-076c2050-e87d-41ae-b0e0-98473102445d" src="https://github.com/user-attachments/assets/2f0cea99-a447-4832-ba0b-f44f34323238" />



## Result:
Thus, the program to display stack elements using linked list is verified successfully. 



# EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
## Aim:
To write a C program to pop an element from the given stack using liked list.

## Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
## Program:
```
 #include <stdio.h>
 #include <stdlib.h>
 struct Node {
 char data[50];
 struct Node *next;
 };
 struct Node *head = NULL;
 void pop() {
 if (head == NULL) {
 printf("Stack is empty.\n");
 } 
else {
 struct Node *temp = head;
 head = head->next;   
free(temp);
 printf("Element popped successfully.\n");
 }
 }
 int main() {
 pop(); 
return 0;
 }
```

## Output:
<img width="722" height="567" alt="517984919-2c203935-b7d9-437a-94a9-0b7379dafd7e" src="https://github.com/user-attachments/assets/80e93938-b7fc-471f-956c-0adc24fad5bd" />


## Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
# EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display queue elements using linked list.
## Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
## Program:
```
 #include <stdio.h>
 #include <stdlib.h>
 struct Node {
 int data;
 struct Node *next;
 };
 struct Node *front = NULL;
  struct Node *rear = NULL;
 void display() {
 struct Node *temp = front;
 if (front == NULL) {
 printf("Queue is empty.\n");
 return;
 }
 printf("Queue elements are:\n");
 while (temp != NULL) {
 printf("%d ", temp->data);
 temp = temp->next;
 }
 printf("\n");
 }
 void enqueue(int value) {
 struct Node *newNode = (struct Node*)malloc(sizeof(struct Node));
 newNode->data = value;
 newNode->next = NULL;
 if (rear == NULL) {
 front = rear = newNode;
 } else {
 rear->next = newNode;
 rear = newNode;
 }
 }
 int main() {
 enqueue(10);
 enqueue(20);
 enqueue(30);
 display();  
}
 return 0;
```
## Output:
<img width="635" height="574" alt="517985304-3b6c6b24-dc2c-4eea-9805-49c2173c2879" src="https://github.com/user-attachments/assets/402d5414-91cb-4eaf-9232-c6fd5a03d41e" />


## Result:
Thus, the program to display queue elements using linked list is verified successfully.

# EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST
## Aim:
To write a C program to insert elements in queue using linked list

## Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
## Program:
```
#include <stdio.h>
#include <stdlib.h>
struct Node {
  int data;
       struct Node *next;
   };
   struct Node *front = NULL;
   struct Node *rear = NULL;
   void enqueue(int value) {
       struct Node *p = (struct Node*)malloc(sizeof(struct Node));
       p->data = value;
       p->next = NULL;
       if (front == NULL) {
           front = rear = p;
       } else {
           rear->next = p;
           rear = p;
       }
       printf("%d inserted into the queue.\n", value);
   }
   void display() {
       struct Node *temp = front;
       if (front == NULL) {
           printf("Queue is empty.\n");
           return;
       }
       printf("Queue elements: ");
       while (temp != NULL) {
           printf("%d ", temp->data);
           temp = temp->next;
       }
       printf("\n");
   }
int main() {
   enqueue(10);
   enqueue(20);
   enqueue(30);
   display();  
   return 0;
}
```
## Output:
<img width="726" height="549" alt="517985691-39abba47-27a2-441d-af05-a96f5cf17522" src="https://github.com/user-attachments/assets/3aec8431-ea82-4e2d-95b5-31cf5352e770" />

## Result:

Thus, the program to insert elements in queue using linked list is verified successfully.



# EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


## Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

## Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

## Program:
```
struct Node
{
   char data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek()
{
    printf("%c",front->data);
}

```
## Output:
<img width="367" height="514" alt="512668214-ba360838-d234-4df4-8a04-769585ad61eb" src="https://github.com/user-attachments/assets/08c91a90-8bf9-4c15-b02e-2c23e439f111" />
ere



## Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


