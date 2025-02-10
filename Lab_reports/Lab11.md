## *CODEFORCES*

## *Number of solves: 15*
## *From 5 February 2025   To        10 February 2025*
<p align="center">
<img alt="code force output image" src="https://github.com/user-attachments/assets/51d5b2e3-80ec-4a67-9ddc-fd16f6435f02"/>
<div align="center"> 
    
[submissions](https://codeforces.com/submissions/joseph)
</div>
</p>




## *Lab No : 11*

## *Lab Workout : Programming Exercises*

## *Submission Date : 11 February, 2025*

---

## *Problem 1 :*
<div align="justify"> Write a program in C to calculate the area and perimeter of two circles using a structure named "Circle". </div>

## *Code :*
~~~C
#include <stdio.h>
#define PI 3.14159

struct Circle {
    float radius;
};

int main() {
    struct Circle c1, c2;
    FILE *file = fopen("test.txt", "w");

    if (file == NULL) {
        printf("Error opening file!\n");
        return 1;
    }
    printf("Enter radius of first circle: ");
    scanf("%f", &c1.radius);
    printf("Enter radius of second circle: ");
    scanf("%f", &c2.radius);
    fprintf(file, "Circle 1 - Area: %.2f, Perimeter: %.2f\n", 3.1416*c1.radius*c1.radius, 2*3.1416*c1.radius);
    fprintf(file, "Circle 2 - Area: %.2f, Perimeter: %.2f\n", 3.1416*c2.radius*c2.radius, 2*3.1416*c2.radius);
    fclose(file);
    return 0;
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/9c95120a-b611-43d9-8776-bfd4b36b6cf3">
</p>
<p align="center">
<img alt="Problem 1 output image" src="https://github.com/user-attachments/assets/8219ceac-a9e6-4b26-80f8-d49140ee0150">
</p>

## *Discussion :*
<div align="justify"> This program defines a structure named "Circle" that holds the radius of a circle. It calculates the area and perimeter for two circles and displays the results. </div>

---

## *Problem 2 :*
<div align="justify"> Write a program in C to store employee details and find the employee with the highest salary. </div>

## *Code :*
~~~C
#include <stdio.h>

struct Employee {
    int id;
    char name[50];
    float salary;
};

int main() {
    struct Employee emp[3], highest;

    for (int i = 0; i < 3; i++) {
        printf("Enter Employee %d ID: ", i + 1);
        scanf("%d", &emp[i].id);
        printf("Enter Employee %d Name: ", i + 1);
        scanf(" %[^\n]", emp[i].name);
        printf("Enter Employee %d Salary: ", i + 1);
        scanf("%f", &emp[i].salary);
        printf("\n");
    }

    highest = emp[0];
    for (int i = 1; i < 3; i++) {
        if (emp[i].salary > highest.salary) {
            highest = emp[i];
        }
    }

    printf("\nEmployee with Highest Salary:\n");
    printf("ID: %d\nName: %s\nSalary: %.2f\n", highest.id, highest.name, highest.salary);

    return 0;
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 2 output image" src="https://github.com/user-attachments/assets/d874dfe0-55ed-48bc-9b56-b7e976067027">
</p>

## *Discussion :*
<div align="justify"> This program defines a structure "Employee" to store employee details. It inputs data for three employees, finds the one with the highest salary, and displays their details. </div>

---

## *Problem 3 :*
<div align="justify"> Write a program in C to calculate the total rental cost of cars using a structure named "Car". </div>

## *Code :*
~~~C
#include <stdio.h>

struct Car {
    int id;
    char model[50];
    float rentalRate;
};

int main() {
    struct Car cars[3];
    int days;

    for (int i = 0; i < 3; i++) {
        printf("Enter Car %d ID: ", i + 1);
        scanf("%d", &cars[i].id);
        printf("Enter Car %d Model: ", i + 1);
        scanf(" %[^\n]", cars[i].model);
        printf("Enter Car %d Rental Rate per day: ", i + 1);
        scanf("%f", &cars[i].rentalRate);
        printf("\n");
    }

    printf("Enter the number of days to rent: ");
    scanf("%d", &days);

    for (int i = 0; i < 3; i++) {
        float totalCost = days * cars[i].rentalRate;
        printf("\nCar ID: %d\nModel: %s\nTotal Rental Cost for %d days: %.2f\n",
               cars[i].id, cars[i].model, days, totalCost);
    }

    return 0;
}

~~~

## *Output :* 
<p align="center">
<img alt="Problem 3 output image" src="https://github.com/user-attachments/assets/e273a473-05d7-4c2d-b917-3cd345fa8cfa">
</p>

## *Discussion :*
<div align="justify"> This program defines a structure "Car" to store car details. It inputs data for three cars and calculates the total rental cost based on user-specified rental days. </div>

---
