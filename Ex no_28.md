# EX 28 C program that demonstrates the use of enum (enumeration) type to define and use named integer constants.
## DATE:19/05/25
## AIM:
To write a C program that demonstrates the use of enum (enumeration) type to define and use named integer constants.

## Algorithm
   
1. Analyze the question
2. Follow the algorithm
3. Try the code
4.  Check for error
5. Run & Display the output
## Program:
```
/*
C program that demonstrates the use of enum (enumeration) type to define and use named integer constants.
Developed by: 
RegisterNumber:  
*/
```
#include <stdio.h>

// Define enum for days of the week
enum Day { SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY };

int main() {
    enum Day today;

    today = WEDNESDAY;

    // Print enum value and its meaning
    printf("Enum value of today is: %d\n", today);

    if (today == WEDNESDAY) {
        printf("It's Wednesday, midweek!\n");
    }

    return 0;
}
## Output:

It's Wednesday, midweek!

## Result:
Thus the program was executed and the output was verified successfully.
