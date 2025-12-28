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
    float length, width, area;
    float *lptr = &length, *wptr = &width, *aptr = &area;

    // Read length and width
    scanf("%f %f", lptr, wptr);

    // Calculate area using pointers
    *aptr = (*lptr) * (*wptr);

    // Print area
    printf("Area of rectangle = %.2f", *aptr);

    return 0;
}
```
## OUTPUT
<img width="566" height="246" alt="image" src="https://github.com/user-attachments/assets/4c818354-1cc3-4c5d-ab35-6bda5519f748" />
		       	


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

int main() {
    char *str;
    int i;

    // Allocate memory for 8 characters (7 + 1 for null terminator)
    str = (char *)malloc(8 * sizeof(char));

    if (str == NULL) {
        printf("Memory not allocated.\n");
        return 1;
    }

    // Assign characters
    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0'; // null terminator

    // Print the string
    printf("%s", str);

    // Free allocated memory
    free(str);

    return 0;
}
```
## OUTPUT
<img width="452" height="185" alt="image" src="https://github.com/user-attachments/assets/ee68a5b1-66fc-447d-8a85-fe000313a9b9" />



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
```
#include <stdio.h>

// Define the structure
struct Student {
    int id;
    char name[50];
    int age;
    float marks;
};

int main() {
    struct Student s;

    // Read student information
    printf("Enter student ID: ");
    scanf("%d", &s.id);

    printf("Enter student name: ");
    scanf(" %[^\n]", s.name);  // To read full name with spaces

    printf("Enter student age: ");
    scanf("%d", &s.age);

    printf("Enter student marks: ");
    scanf("%f", &s.marks);

    // Display student information
    printf("\nStudent Information:\n");
    printf("ID: %d\n", s.id);
    printf("Name: %s\n", s.name);
    printf("Age: %d\n", s.age);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}
```

## OUTPUT
<img width="420" height="433" alt="image" src="https://github.com/user-attachments/assets/2cc48678-08c6-457a-a4c2-749165190461" />


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

struct Employee {
    int id;
    char name[50];
    float basic, hra, da, gross;
};

int main() {
    struct Employee e[3];
    int i;

    // Read details of 3 employees
    for (i = 0; i < 3; i++) {
        printf("\nEnter details of Employee %d\n", i + 1);

        printf("ID: ");
        scanf("%d", &e[i].id);

        printf("Name: ");
        scanf(" %[^\n]", e[i].name);

        printf("Basic Salary: ");
        scanf("%f", &e[i].basic);

        printf("HRA: ");
        scanf("%f", &e[i].hra);

        printf("DA: ");
        scanf("%f", &e[i].da);

        // Calculate Gross Salary
        e[i].gross = e[i].basic + e[i].hra + e[i].da;
    }

    // Display employee details with gross salary
    printf("\nEmployee Details with Gross Salary:\n");
    for (i = 0; i < 3; i++) {
        printf("\nEmployee %d\n", i + 1);
        printf("ID: %d\n", e[i].id);
        printf("Name: %s\n", e[i].name);
        printf("Gross Salary: %.2f\n", e[i].gross);
    }

    return 0;
}
```
 ## OUTPUT
<img width="362" height="651" alt="image" src="https://github.com/user-attachments/assets/394ca79f-50a9-4bec-a5c9-e53ff5e11672" />
<img width="382" height="545" alt="image" src="https://github.com/user-attachments/assets/cc866fb4-ea05-43e1-b9ed-853a34096308" />

 

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

struct Student {
    int id;
    char name[50];
    float marks[3];
};

int main() {
    struct Student s;
    float total = 0, avg;
    int i;

    // Read student details
    printf("Enter Student ID: ");
    scanf("%d", &s.id);

    printf("Enter Student Name: ");
    scanf(" %[^\n]", s.name);

    printf("Enter marks in 3 subjects:\n");
    for (i = 0; i < 3; i++) {
        scanf("%f", &s.marks[i]);
        total += s.marks[i];
    }

    // Calculate average
    avg = total / 3;

    // Display result
    printf("Total = %.2f\n", total);
    printf("Average = %.2f\n", avg);

    return 0;
}
```

## OUTPUT
<img width="462" height="382" alt="image" src="https://github.com/user-attachments/assets/1195dd71-4e41-4de3-9224-c3bbd1c8f1a5" />

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


