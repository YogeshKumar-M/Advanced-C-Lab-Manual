# EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
## Aim:
To write a C program print the lowercase English word corresponding to the number
## Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
## Program:
```
#include <stdio.h>

int main() {
    int n;

    printf("Enter a number (71-79): ");
    scanf("%d", &n);

    switch(n) {
        case 71:
            printf("seventy one");
            break;
        case 72:
            printf("seventy two");
            break;
        case 73:
            printf("seventy three");
            break;
        case 74:
            printf("seventy four");
            break;
        case 75:
            printf("seventy five");
            break;
        case 76:
            printf("seventy six");
            break;
        case 77:
            printf("seventy seven");
            break;
        case 78:
            printf("seventy eight");
            break;
        case 79:
            printf("seventy nine");
            break;
        default:
            printf("Invalid input");
    }

    return 0;
}
```



## Output:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/f30be44e-8dc5-4b7b-9e44-289e9b336e9c" />


## Result:
Thus, the program is verified successfully
 
# EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
## Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
## Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
## Program:
```
#include <stdio.h>
#include <string.h>

int main() {
    char a[50];
    int i, j, count;

    printf("Enter a number: ");
    scanf("%s", a);

    for(i = 0; i <= 9; i++) {
        count = 0;

        for(j = 0; a[j] != '\0'; j++) {
            if(a[j] == i + '0') {
                count++;
            }
        }

        printf("%d ", count);
    }

    return 0;
}
```



## Output:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/e1b5d317-9c81-45e3-a903-20b89b1fd0a4" />

## Result:
Thus, the program is verified successfully

# EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
## Aim:
To write a C program to print all of its permutations in strict lexicographical order.

## Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
## Program:
```
#include <stdio.h>
#include <string.h>

// Function to swap characters
void swap(char *a, char *b) {
    char temp = *a;
    *a = *b;
    *b = temp;
}

// Function to reverse substring
void reverse(char str[], int start, int end) {
    while(start < end) {
        swap(&str[start], &str[end]);
        start++;
        end--;
    }
}

int main() {
    char str[100];
    int i, j, len;

    printf("Enter a string: ");
    scanf("%s", str);

    len = strlen(str);

    // Step 1: Sort the string
    for(i = 0; i < len - 1; i++) {
        for(j = i + 1; j < len; j++) {
            if(str[i] > str[j]) {
                swap(&str[i], &str[j]);
            }
        }
    }

    // Step 2: Print first permutation
    printf("%s\n", str);

    // Step 3: Generate permutations
    while(1) {
        // Find i
        for(i = len - 2; i >= 0; i--) {
            if(str[i] < str[i + 1])
                break;
        }

        if(i < 0)
            break;

        // Find j
        for(j = len - 1; j > i; j--) {
            if(str[j] > str[i])
                break;
        }

        // Swap
        swap(&str[i], &str[j]);

        // Reverse
        reverse(str, i + 1, len - 1);

        // Print
        printf("%s\n", str);
    }

    return 0;
}
```



## Output:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/e0fb26cb-01f0-48b6-b7f2-0dbf86b0b22e" />

## Result:
Thus, the program is verified successfully
 
# EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
## Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
## Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
## Program:
```
#include <stdio.h>

int main() {
    int n, i, j, min, len;
printf("Enter n: ");
scanf("%d", &n);
len = n * 2 - 1;
for (i = 0; i < len; i++) {
    for (j = 0; j < len; j++) {

        min = i;
        if (j < min) min = j;
        if (len - 1 - i < min) min = len - 1 - i;
        if (len - 1 - j < min) min = len - 1 - j;
        printf("%d ", n - min);
    }
    printf("\n");
}
return 0;
}
```

## Output:
<img width="1495" height="1050" alt="496962791-baa1fad6-13d6-4bc1-871c-75cbe6322ed6" src="https://github.com/user-attachments/assets/934e5312-c850-48da-8b26-191d6338cffe" />

## Result:
Thus, the program is verified successfully

# EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

## Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

## Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

## Program:
```
#include <stdio.h>
int square() 
{
    int num;   
    printf("Enter a number: ");
    scanf("%d", &num);

    return num * num;
}
int main() 
{
    int result;
    result = square();
    printf("Square is: %d\n", result);
    return 0;
}
```
## Output:

<img width="1687" height="1083" alt="496963316-424cf80b-0138-4e3d-ab93-25404e8aeabc" src="https://github.com/user-attachments/assets/9b4c0143-52e8-4b8d-b899-5698b6d869a7" />

## Result:
Thus, the program is verified successfully



























