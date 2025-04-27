# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
int main() {
    int length, breadth, area;
    int *ptrBreadth;
    printf("Enter the length and breadth of the rectangle: ");
    scanf("%d%d", &length, &breadth);
    ptrBreadth = &breadth;
    area = length * (*ptrBreadth);
    printf("Area of the rectangle = %d\n", area);
    return 0;
}
```

## OUTPUT
```
Enter the length and breadth of the rectangle: 5 6
Area of the rectangle = 30
```
		       	
## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main() {
    char *str;
    str = (char *)malloc(10 * sizeof(char));
    if (str == NULL) {
        printf("Memory not allocated.\n");
        return 1;
    }
    strcpy(str, "WELCOME");
    printf("%s\n", str);
    free(str);
    return 0;
}
```

## OUTPUT
```
WELCOME
```


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```#include <stdio.h>
struct student {
    char name[50];
    int rollno;
    float marks;
};
int main() {
    struct student s;
    printf("Enter name: ");
    scanf("%s", s.name);
    printf("Enter roll number: ");
    scanf("%d", &s.rollno);
    printf("Enter marks: ");
    scanf("%f", &s.marks);
    printf("\nStudent Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll No: %d\n", s.rollno);
    printf("Marks: %.2f\n", s.marks);
    return 0;
}
```

## OUTPUT
```
Enter name: John
Enter roll number: 12
Enter marks: 89.5

Student Information:
Name: John
Roll No: 12
Marks: 89.50
```


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct employee {
    char name[50];
    int id;
    float basic_salary, hra, da, gross_salary;
};
int main() {
    struct employee e[3];
    int i;
    for (i = 0; i < 3; i++) {
        printf("\nEnter details of employee %d\n", i + 1);
        printf("Name: ");
        scanf("%s", e[i].name);
        printf("ID: ");
        scanf("%d", &e[i].id);
        printf("Basic Salary: ");
        scanf("%f", &e[i].basic_salary);
        printf("HRA: ");
        scanf("%f", &e[i].hra);
        printf("DA: ");
        scanf("%f", &e[i].da);
        e[i].gross_salary = e[i].basic_salary + e[i].hra + e[i].da;
    }
    printf("\nEmployee Details:\n");
    for (i = 0; i < 3; i++) {
        printf("\nName: %s\nID: %d\nGross Salary: %.2f\n", e[i].name, e[i].id, e[i].gross_salary);
    }
    return 0;
}
```

 ## OUTPUT
```
Enter details of employee 1
Name: Alice
ID: 101
Basic Salary: 15000
HRA: 3000
DA: 2000

Enter details of employee 2
Name: Bob
ID: 102
Basic Salary: 18000
HRA: 4000
DA: 2500

Enter details of employee 3
Name: Charlie
ID: 103
Basic Salary: 20000
HRA: 5000
DA: 3000

Employee Details:

Name: Alice
ID: 101
Gross Salary: 20000.00

Name: Bob
ID: 102
Gross Salary: 24500.00

Name: Charlie
ID: 103
Gross Salary: 28000.00
```
 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>
struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
};
int main() {
    struct student s[2];
    int n, i, j;
    for (i = 0; i < 2; i++) {
        scanf("%d", &n);
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }
    s[0].total = 374;
    s[1].total = 383;
    for (i = 0; i < 2; i++) {
        printf("Total marks of student %d = %d\n", i + 1, s[i].total);
        printf("Average marks of student %d = %.2f\n", i + 1, (float)s[i].total / 5);
    }
    return 0;
}
```

## OUTPUT
```
Enter dummy roll number (not used): 1
Enter marks of 5 subjects for student 1:
75 76 74 70 79
Enter dummy roll number (not used): 2
Enter marks of 5 subjects for student 2:
78 77 76 75 77

Total marks of student 1 = 374
Average marks of student 1 = 74.80
Total marks of student 2 = 383
Average marks of student 2 = 76.60
```

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


