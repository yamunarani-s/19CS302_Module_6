# EX 26 C program demonstrating a self-referential structure where an employee has a pointer to their manager.
## DATE:19/05/25
## AIM:
To write a C program to demonstrate a self-referential structure where an employee has a pointer to their manager.

## Algorithm
1. Analyze the question
2. Follow the algorithm
3. Try the code
4.  Check for error
5. Run & Display the output
## Program:
```
/*
C program demonstrating a self-referential structure where an employee has a pointer to their manager.
Developed by: 
RegisterNumber:  
*/
```
#include <stdio.h>
#include <string.h>

// Define a structure for Employee
struct Employee {
    int emp_id;
    char name[50];
    struct Employee *manager;  // Pointer to another Employee (manager)
};

int main() {
    struct Employee e1, e2;

    // Initialize manager (e1)
    e1.emp_id = 1001;
    strcpy(e1.name, "Alice");
    e1.manager = NULL;  // Alice has no manager (e.g., CEO)

    // Initialize employee (e2)
    e2.emp_id = 1002;
    strcpy(e2.name, "Bob");
    e2.manager = &e1;   // Bob's manager is Alice

    // Display details
    printf("Employee Name: %s\n", e2.name);
    printf("Employee ID  : %d\n", e2.emp_id);

    if (e2.manager != NULL) {
        printf("Manager Name : %s\n", e2.manager->name);
        printf("Manager ID   : %d\n", e2.manager->emp_id);
    } else {
        printf("This employee has no manager.\n");
    }

    return 0;
}


## Output:

Employee Name: Bob
Employee ID  : 1002
Manager Name : Alice
Manager ID   : 1001


## Result:
Thus the program was executed and the output was verified successfully.
