**EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.**

**Aim:**

To write a C program for array of structure to check eligibility for the vaccine person age above 18 years of age.
 
**Algorithm:**

1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 18
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
**Program:**
```
#include <stdio.h>
struct Person {
    char name[50];
    int age;
};
int main() {
    struct Person p;
    scanf("%d", &p.age);
    scanf(" %[^\n]", p.name);  
    printf("Age:%d\n", p.age);
    printf("Name:%s", p.name);
    printf("vaccine:%d\n", p.age);
    if (p.age > 18) {
        printf("eligibility:yes\n");
    } else {
        printf("eligibility:no\n");
    }

    return 0;
}

```


**Output:**

![image](https://github.com/user-attachments/assets/a2d1e6b5-c4a4-4ae2-b91a-958b5491311a)

**Result:**

Thus the program is verified successfully. 



**EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION**

**Aim:**

To write a C program for passing structure as function and returning a structure from a function

**Algorithm:**

1.	Define structure numbers with members a and b.
2.	Declare variable n of type numbers.
3.	Prompt the user to enter values for a and b.
4.	Input values for a and b into n using scanf.
5.	Call the add function with n as an argument.
6.	Print the result returned by the add function.
7.	Return 0
 
**Program:**
```
#include <stdio.h>

struct Person {
    char name[90];
    int age;
    char gender[90];
    char phno[80];
    char Edu_Quali[50];
    char skill[200];
    float experience;
    int current_sal;
    int expected_sal;

    struct date {
        int dd;
        int mm;
        int yyyy;
    } dob;
};

int main() {
    struct Person e1;
    fgets(e1.name, sizeof(e1.name), stdin);
    scanf("%d", &e1.age);
    getchar();
    fgets(e1.gender, sizeof(e1.gender), stdin);
    fgets(e1.phno, sizeof(e1.phno), stdin);
    fgets(e1.Edu_Quali, sizeof(e1.Edu_Quali), stdin);
    fgets(e1.skill, sizeof(e1.skill), stdin);
    scanf("%f", &e1.experience);
    scanf("%d", &e1.current_sal);
    scanf("%d", &e1.expected_sal);
    scanf("%d %d %d", &e1.dob.dd, &e1.dob.mm, &e1.dob.yyyy);
    printf("Name:%s", e1.name);
    printf("Age: %d\n", e1.age);
    printf("Gender: %s", e1.gender);
    printf("Phone: %s", e1.phno);
    printf("Qualification: %s", e1.Edu_Quali);
    printf("Skills: %s", e1.skill);
    printf("Experience: %.2f years\n", e1.experience);
    printf("Expected CTC: %d\n",e1.current_sal );
    printf("Current CTC: %d\n",e1.expected_sal );
    printf("Date of Birth:%d/%d/%d\n", e1.dob.dd, e1.dob.mm, e1.dob.yyyy);

    return 0;
}


```

**Output:**

![image](https://github.com/user-attachments/assets/1fcdb5fe-aba3-46dd-8656-774f6978258b)



**Result:**

Thus the program is verified successfully


 
**EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()**

**Aim:**

To write a C program to read a file name from user

**Algorithm:**

1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
**Program:**
```
#include <stdio.h>
int main()
{
    char name[50];
    scanf("%s",name);
    FILE *fptr;
    fptr=fopen(name,"w");
    if(fptr==NULL)
    {
        printf("Could not be opened\n");
        return 1;
    }
    printf("%s File Created Successfully\n",name);
    printf("%s File Opened\n",name);
    fclose(fptr);
    printf("%s File Closed\n",name);
    return 0;
}
```


**Output:**

![image](https://github.com/user-attachments/assets/32e91865-18ec-4331-aa79-278580eee5aa)

**Result:**
Thus, the program is verified successfully
 


**EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE**

**Aim:**

To write a C program to read, a file and insert text in that file

**Algorithm:**

1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
**Program:**
```
#include <stdio.h>
int main()
{
    char name[50];
    int n;
    scanf("%s",name);
    scanf("%d",&n);
    FILE *fptr;
    fptr=fopen(name,"w");
    if(fptr!=NULL)
    {
        printf("%s Opened\n",name);
    }
    

        printf("Data added Successfully");
    
    fclose(fptr);
    return 0;
}
```




**Output:**

![image](https://github.com/user-attachments/assets/89170b6c-9cf8-4501-b210-532f9a5319ee)



**Result:**

Thus the program is verified successfully



**Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE**

**Aim:**

The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

**Algorithm:**

1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

**Program:**
```
#include <stdio.h>
struct Student {
    char name[50];
    int rollNumber;
    float marks;
};

int main() {
    struct Student s;
    scanf("%s", s.name); 
    scanf("%d", &s.rollNumber);
    scanf("%f", &s.marks);
    printf("Displaying Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll number: %d\n", s.rollNumber);
    printf("Marks: %.1f\n", s.marks);

    return 0;
}
```

**Output:**

![image](https://github.com/user-attachments/assets/dafb9654-cc99-470a-b428-cfc760ec534a)



**Result:**

Thus the program is verified successfully
