// C program to demonstrate the array of structures 
#include <stdio.h> 
  
// structure template 
struct Employee { 
    char Name[20]; 
    int employeeID; 
    int WeekAttendence[7]; 
}; 
  
// driver code 
int main() 
{ 
    // defining array of structure of type Employee 
    struct Employee emp[5]; 
  
    // adding data 
    for (int i = 0; i < 5; i++) { 
        emp[i].employeeID = i; 
        strcpy(emp[i].Name, "Amit"); 
        int week; 
        for (week = 0; week < 7; week++) { 
            int attendence; 
            emp[i].WeekAttendence[week] = week; 
        } 
    } 
    printf("\n"); 
  
    // printing data 
    for (int i = 0; i < 5; i++) { 
        printf("Emplyee ID: %d - Employee Name: %s\n", 
               emp[i].employeeID, emp[i].Name); 
        printf("Attendence\n"); 
        int week; 
        for (week = 0; week < 7; week++) { 
            printf("%d ", emp[i].WeekAttendence[week]); 
        } 
        printf("\n"); 
    } 
  
    return 0; 
}
