# -a-C-program-that-defines-a-structure-employee-
#include <stdio.h>

// Define the structure to hold employee details
struct Employee {
    int empno;
    char empname[50];
    char department[50];
    float salary;
};

// Function to display employee details
void displayEmployees(struct Employee employees[], int count) {
    printf("EmpNo\tName\t\tDepartment\tSalary\n");
    printf("------------------------------------------------------\n");
    for (int i = 0; i < count; i++) {
        printf("%d\t%-15s\t%-15s\t%.2f\n", employees[i].empno, employees[i].empname, employees[i].department, employees[i].salary);
    }
}

int main() {
    // Create an array to store 20 employees
    struct Employee employees[20];

    // Input details for 3 employees (for example)
    employees[0].empno = 1;
    snprintf(employees[0].empname, sizeof(employees[0].empname), "Chirag");
    snprintf(employees[0].department, sizeof(employees[0].department), "HR");
    employees[0].salary = 20000;

    employees[1].empno = 2;
    snprintf(employees[1].empname, sizeof(employees[1].empname), "Arnav");
    snprintf(employees[1].department, sizeof(employees[1].department), "Finance");
    employees[1].salary = 56000;

    employees[2].empno = 3;
    snprintf(employees[2].empname, sizeof(employees[2].empname), "Shivam");
    snprintf(employees[2].department, sizeof(employees[2].department), "IT");
    employees[2].salary = 30500;

    // Display employee details
    displayEmployees(employees, 3);

    return 0;
}
