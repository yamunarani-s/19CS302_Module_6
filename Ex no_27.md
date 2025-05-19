# EX 27 C program that demonstrates the use of typedef to create a new alias name for a data type.
## DATE:19/05/25
## AIM:
To write a C program that demonstrates the use of typedef to create a new alias name for a data type.

## Algorithm
1. Analyze the question
2. Follow the algorithm
3. Try the code
4.  Check for error
5. Run & Display the output 

## Program:
```
/*
C program that demonstrates the use of typedef to create a new alias name for a data type.
Developed by: 
RegisterNumber:  
*/
``
```
#include <stdio.h>

// Creating aliases using typedef
typedef unsigned int uint;
typedef float real;
typedef struct {
    int emp_id;
    char name[50];
} Employee;

int main() {
    uint age = 25;         // alias for unsigned int
    real salary = 55000.5; // alias for float

    Employee e1;           // alias for struct Employee
    e1.emp_id = 101;
    snprintf(e1.name, sizeof(e1.name), "John");

    // Display values
    printf("Age      : %u\n", age);
    printf("Salary   : %.2f\n", salary);
    printf("Employee ID : %d\n", e1.emp_id);
    printf("Employee Name : %s\n", e1.name);

    return 0;
}`

## Output:
Age      : 25
Salary   : 55000.50
Employee ID : 101
Employee Name : John

## Result:
Thus the program was executed and the output was verified successfully.
