# EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.
## Aim:
To write a C program to display stack elements using an array.
## Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
## Program:
```
#include <stdio.h>
 #include <stdlib.h>
 #define SIZE 5   
int stack[SIZE];
 int top = -1;
 void display() {
    if (top == -1) {
        printf("Stack is empty\n");
        return;
    }
    printf("Stack contents: ");
    for (int i = top; i >= 0; i--) {
        printf("%d ", stack[i]);
    }
    printf("\n");
 }
 void push(int value) {
    if (top == SIZE - 1) {
        printf("Stack Overflow! Cannot push %d\n", value);
        return;
    }
    stack[++top] = value;
    printf("%d pushed into stack\n", value);
 }
 void pop() {
    if (top == -1) {
        printf("Stack Underflow! Cannot pop\n");
        return;
    }
    printf("%d popped from stack\n", stack[top--]);
 }
 int main() {
    int choice, value;
 while (1) {
    printf("\n--- Stack Menu ---\n");
    printf("1. Push\n2. Pop\n3. Display\n4. Exit\n");
    printf("Enter choice: ");
    scanf("%d", &choice);
    switch (choice) {
        case 1:
            printf("Enter value to push: ");
            scanf("%d", &value);
            push(value);
            break;
        case 2:
            pop();
             break;
case 3:
display();
break;
case 4:
exit(0);
default:
printf("Invalid choice!\n");
}
}
return 0;
}
```
## Output:
<img width="1570" height="919" alt="517973112-b55d0664-d211-43ae-a461-57af44981230" src="https://github.com/user-attachments/assets/9b131e2d-4dc8-4d60-8738-7b14d87fcdf5" />

## Result:
Thus, the program to display stack elements using an array is verified successfully.
 

# EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
## Aim:
To create a C program to push the given element in to a stack using array.
## Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
## Program:
```
 #include <stdio.h>
 #define SIZE 5  
float stack[SIZE];
 int top = -1;
 void push(float value) 
{
 if (top == SIZE - 1) {
 printf("Stack Overflow! Cannot push %.2f\n", value);
 return;
 }
 stack[++top] = value;
 printf("%.2f pushed into stack\n", value);
 }
 int main() {
 // Stack already initialized with top = -1
 push(10.5);
 push(20.75);
 push(30.1);
 printf("\nCurrent stack contents:\n");
 for (int i = top; i >= 0; i--) {
 printf("%.2f ", stack[i]);
 }
 printf("\n");
 return 0;
 }
```
## Output:
<img width="1209" height="765" alt="517973507-08a4b3b8-61f1-4b77-a259-bcbf5c485f10" src="https://github.com/user-attachments/assets/b35f41a4-c14a-410f-ad1a-cc24ae893f60" />

## Result:
Thus, the program to push the given element in to a stack using array is verified successfully
 
# EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
## Aim:
To write a C program to display queue elements using array

## Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
## Program:
```
 #include <stdio.h>
 #include <stdlib.h>
 #define SIZE 5
 int queue[SIZE];
 int front = -1, rear = -1;
 void display() {
 if (front == -1) {
 printf("Queue is empty\n");
 return;
 }
 printf("Queue contents: ");
 for (int i = front; i <= rear; i++) {
 printf("%d ", queue[i]);
 }
 printf("\n");
 }
 void enqueue(int value) {
 if (rear == SIZE - 1) {
 printf("Queue Overflow! Cannot insert %d\n", value);
 return;
 }
 if (front == -1) front = 0; 
queue[++rear] = value;
 printf("%d enqueued into queue\n", value);
 }
 void dequeue() {
 if (front == -1 || front > rear) {
 printf("Queue Underflow! Cannot dequeue\n");
 return;
 }
 printf("%d dequeued from queue\n", queue[front++]);
 if (front > rear) { 
front = rear = -1;
 }
 }
 int main() {
 enqueue(10);
 enqueue(20);
 enqueue(30);
 display();
 dequeue();
 display();
 enqueue(40);
 enqueue(50);
 enqueue(60);
 display();
 return 0;
 }
```
## Output:

<img width="1529" height="932" alt="517973692-26f04692-49e9-4de6-ac7f-7ed496c3f375" src="https://github.com/user-attachments/assets/40d827b0-b8d1-41e7-b717-3ab8ca14f6cb" />


## Result:
Thus, the program to display queue elements using array is verified successfully.


 
# EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
## Aim:
To write a C program to insert elements in queue using array.

## Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

## Program:
```
 #include <stdio.h>
 #include <stdlib.h>
 #define SIZE 5  
float queue[SIZE];
 int front = -1, rear = -1;
 void enqueue(float value) {
 if (rear == SIZE - 1) {
 printf("Queue Overflow! Cannot insert %.2f\n", value);
 return;
 }
 if (front == -1) front = 0;  
queue[++rear] = value;
 printf("%.2f enqueued into queue\n", value);
 }
 int main() {
 enqueue(10.5);
 enqueue(20.25);
 enqueue(30.75);
 enqueue(40.0);
 enqueue(50.99);
 enqueue(60.6);  
return 0;
 }
```
## Output:
<img width="904" height="563" alt="517973952-c9777fa3-6234-4e9f-a3d4-5476ff9934e9" src="https://github.com/user-attachments/assets/32eb193c-5a45-4566-babb-53b376e941cb" />

## Result:
Thus, the program to insert elements in queue using array is verified successfully.
 
# EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY
## Aim:

To create a function in C that deletes an element from a queue implemented using an array.

## Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



## Program:
```
 #include <stdio.h>
 #include <stdlib.h>
 #define SIZE 5
 float queue[SIZE];
 int front = -1, rear = -1;
 void enqueue(float value) {
 if (rear == SIZE - 1) {
 printf("Queue Overflow! Cannot insert %.2f\n", value);
 return;
 }
 if (front == -1) front = 0; 
queue[++rear] = value;
 printf("%.2f enqueued\n", value);
 }
 void dequeue() 
{
 if (front == -1) {
 printf("Queue Underflow! Nothing to delete.\n");
 return;
 }
  printf("%.2f dequeued\n", queue[front]);
 front++;
 if (front > rear) {
 front = rear = -1; 
}
 }
 int main() {
 enqueue(10.5);
 enqueue(20.25);
 enqueue(30.75);
 dequeue(); 
dequeue(); 
dequeue(); 
dequeue(); 
return 0;
 }
```
## Output:

<img width="930" height="574" alt="517974340-7ec058b3-69c5-4cae-998c-5c7260bffd04" src="https://github.com/user-attachments/assets/0d1d8349-e0b1-4963-8aae-cdfe8c399c97" />


## Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
