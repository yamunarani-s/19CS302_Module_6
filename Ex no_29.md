# EX 29 C program to create two float variables using calloc() and find minimum among them.
## DATE:19/05/25
## AIM:
To write a C program to create two float variables using calloc() and find minimum among them.

## Algorithm:
1. Analyze the question
2. Follow the algorithm
3. Try the code
4.  Check for error
5. Run & Display the output

## Program:
```
/*
C program to create two float variables using calloc() and find minimum among them.
Developed by: 
RegisterNumber:  
*/
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    float *a, *b;

    // Allocate memory using calloc
    a = (float *)calloc(1, sizeof(float));
    b = (float *)calloc(1, sizeof(float));

    if (a == NULL || b == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }
    scanf("%f", a);
    scanf("%f", b);
    if (*a < *b) {
        printf("Minimum value is: %.2f\n", *a);
    } else {
        printf("Minimum value is: %.2f\n", *b);
    }

    // Free allocated memory
    free(a);
    free(b);

    return 0;
}

## Output:
Minimum value is: 3.40


## Result:
Thus the program was executed and the output was verified successfully.
