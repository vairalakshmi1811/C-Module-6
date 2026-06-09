## Structures: EB Bill Calculation (C Program)
## Aim
Create a C program using a structure to calculate the electricity bill (EB bill) for 3 customers based on their electricity usage.

## Algorithm
Step 1: Input: Read customer number, previous reading, and current reading for 3 customers into an array of structures e.

Step 2: Calculate Bill: Calculate the units consumed by subtracting previous reading from current reading.

Step 3: Apply billing rates:

    First 100 units: ₹2 per unit

    101 to 200 units: ₹3 per unit

    Above 200 units: ₹5 per unit

Step 4:Output: Display customer number and the calculated bill amount for each customer

## Program
```
#include <stdio.h>
struct Customer {
    int customer_no;
    int prev_reading;
    int curr_reading;
    int units;
    float bill;
};
float calculate_bill(int units) {
    float amount = 0;
    if (units <= 100) {
        amount = units * 2;
    } else if (units <= 200) {
        amount = 100 * 2 + (units - 100) * 3;
    } else {
        amount = 100 * 2 + 100 * 3 + (units - 200) * 5;
    }
    return amount;
}
int main() {
    struct Customer e[3];
    int i;
    for (i = 0; i < 3; i++) {
        printf("Enter details for Customer %d:\n", i + 1);
        printf("Customer Number: ");
        scanf("%d", &e[i].customer_no);
        printf("Previous Reading: ");
        scanf("%d", &e[i].prev_reading);
        printf("Current Reading: ");
        scanf("%d", &e[i].curr_reading);
        e[i].units = e[i].curr_reading - e[i].prev_reading;
        e[i].bill = calculate_bill(e[i].units);
    }
    printf("\nElectricity Bill Summary:\n");
    printf("Customer No\tUnits Consumed\tBill Amount (₹)\n");
    for (i = 0; i < 3; i++) {
        printf("%d\t\t%d\t\t%.2f\n", e[i].customer_no, e[i].units, e[i].bill);
    }
    return 0;
}
```

## Output
<img width="891" height="694" alt="image" src="https://github.com/user-attachments/assets/16027a9d-5555-40a8-a399-a26169d506b8" />

## Result
C program using a structure to calculate the electricity bill (EB bill) for 3 customers based on their electricity usage is created.
