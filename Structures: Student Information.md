## Structures: Student Information Storage (C Program)
## Aim
Create a C program to store and display the information of 5 students using an array of structures.

## Algorithm
1. Input: Read the name and marks of 5 students into an array of structures s.

2. Display Information:

    Iterate through the array and print the roll number, name, and marks for each student.

3.End the program execution.

## Program
```
#include <stdio.h>
struct student {
    int roll_no;
    char name[50];
    float marks;
};

int main() {
    struct student s[5];
    int i;
    for(i = 0; i < 5; i++) {
        printf("\nEnter details of student %d:\n", i + 1);

        printf("Roll Number: ");
        scanf("%d", &s[i].roll_no);

        printf("Name: ");
        scanf("%s", s[i].name);

        printf("Marks: ");
        scanf("%f", &s[i].marks);
    }
    printf("\n--- Student Details ---\n");
    for(i = 0; i < 5; i++) {
        printf("Roll No: %d\n", s[i].roll_no);
        printf("Name: %s\n", s[i].name);
        printf("Marks: %.2f\n\n", s[i].marks);
    }

    return 0;
}
```
## Output
<img width="236" height="770" alt="image" src="https://github.com/user-attachments/assets/3d1ff77d-e087-4fbe-9e97-433f286382f4" />

## Result
C program to store and display the information of 5 students using an array of structures is created.
