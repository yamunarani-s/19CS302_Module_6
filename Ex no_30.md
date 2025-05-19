# EX 30 C program to add two integer elements in an array using realloc() and that array already has three elements.
## DATE:19/05/25
## AIM:
To write a C program to add two integer elements in an array using realloc() and that array already has three elements.

## Algorithm
1. Analyze the question
2. Follow the algorithm
3. Try the code
4.  Check for error
5. Run & Display the output

## Program:
```
/*
C program to add two integer elements in an array using realloc() and that array already has three elements.

Developed by: 
RegisterNumber:  
*/
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int *arr;
    int initial_size = 3;
    int new_elements = 2;
    int total_size = initial_size + new_elements;

    // Allocate memory for initial 3 elements
    arr = (int *)malloc(initial_size * sizeof(int));
    if (arr == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }

    // Initialize the first 3 elements
    arr[0] = 10;
    arr[1] = 20;
    arr[2] = 30;

    printf("Initial array elements: ");
    for (int i = 0; i < initial_size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    // Reallocate memory to hold 5 elements
    arr = (int *)realloc(arr, total_size * sizeof(int));
    if (arr == NULL) {
        printf("Memory reallocation failed\n");
        return 1;
    }

    // Add two new elements
    arr[3] = 40;
    arr[4] = 50;

    printf("Array after adding two elements: ");
    for (int i = 0; i < total_size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    // Add the two new elements
    int sum = arr[3] + arr[4];
    printf("Sum of the two new elements: %d\n", sum);

    // Free the allocated memory
    free(arr);

    return 0;
}


## Output:

Initial array elements: 10 20 30 
Array after adding two elements: 10 20 30 40 50 
Sum of the two new elements: 90


## Result:
Thus the program was executed and the output was verified successfully.
