## Structures: Employee Gross Salary Calculation (C Program)
## Aim
Write a C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structures.

## Algorithm
Step 1: Start the program.

Step 2: Create a structure employee with members: name, id, and salary.

Step 3: Input: Using a structure array, read the name, ID, and basic salary for 3 employees.

Step 4: Calculate: Compute the Gross Salary based on a predefined formula (e.g., adding allowances like DA, HRA, etc., if applicable) or by using basic salary as gross salary if no formula is given.

Step 5: Output: Display employee details including name, ID, and calculated Gross Salary.

Step 6: Stop the program.

## Program 
```
#include <stdio.h>
struct Employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};
int main() {
    struct Employee emp[3];
    int i;
    for (i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);
        printf("Name: ");
        scanf(" %[^\n]", emp[i].name); 
        printf("ID: ");
        scanf("%d", &emp[i].id);
        printf("Basic Salary: ");
        scanf("%f", &emp[i].basic_salary);
        float hra = 0.20f * emp[i].basic_salary;
        float da = 0.80f * emp[i].basic_salary;
        emp[i].gross_salary = emp[i].basic_salary + hra + da;
    }
    printf("Employee Details with Gross Salary:\n");
    printf("Name\t\tID\tBasic Salary\tGross Salary\n");
    for (i = 0; i < 3; i++) {
        printf("%-15s %-5d %-13.2f %.2f\n",
               emp[i].name, emp[i].id, emp[i].basic_salary, emp[i].gross_salary);
    }
    return 0;
}
```

## Output
<img width="890" height="643" alt="image" src="https://github.com/user-attachments/assets/203ace09-e1d1-4bcc-9c7b-8f4aa18e3995" />

## Result
C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structures is written.
