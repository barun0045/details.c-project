#include <stdio.h>
#include <string.h>

// Define a structure (custom data type) for a student record
struct Student {
    int rollNumber;
    char name[50];
    float marks;
};

// Global array to store student records (max 10 students)
struct Student records[10];
int recordCount = 0;

// Function to add a new student record
void addRecord() {
    if (recordCount >= 10) {
        printf("Record limit reached (Max 10 students).\n");
        return;
    }

    printf("\n--- Add New Student ---\n");
    
    printf("Enter Roll Number: ");
    // Check for successful integer input
    if (scanf("%d", &records[recordCount].rollNumber) != 1) {
        printf("Invalid input for Roll Number.\n");
        while (getchar() != '\n'); // Clear buffer
        return;
    }
    
    // Clear the input buffer after reading the integer
    while (getchar() != '\n'); 
    
    printf("Enter Name: ");
    // Read the name and store it
    fgets(records[recordCount].name, 50, stdin);
    // Remove the newline character added by fgets
    records[recordCount].name[strcspn(records[recordCount].name, "\n")] = 0;

    printf("Enter Marks (out of 100): ");
    if (scanf("%f", &records[recordCount].marks) != 1) {
         printf("Invalid input for Marks.\n");
         while (getchar() != '\n'); // Clear buffer
         return;
    }
    
    // Clear the input buffer
    while (getchar() != '\n'); 

    recordCount++;
    printf("✅ Student record added successfully!\n");
}

// Function to display all student records
void viewRecords() {
    if (recordCount == 0) {
        printf("\nNo student records available.\n");
        return;
    }

    printf("\n--- Student Records (%d total) ---\n", recordCount);
    printf("-----------------------------------\n");
    
    // Loop through the stored records
    for (int i = 0; i < recordCount; i++) {
        printf("Roll No: %d, Name: %s, Marks: %.2f\n", 
               records[i].rollNumber, 
               records[i].name, 
               records[i].marks);
    }
    printf("-----------------------------------\n");
}

// Main function with the menu loop
int main() {
    int choice;

    do {
        printf("\n--- Student Management System ---\n");
        printf("1. Add Record\n");
        printf("2. View All Records\n");
        printf("3. Exit\n");
        printf("Enter your choice: ");

        if (scanf("%d", &choice) != 1) {
            printf("Invalid choice. Please enter a number.\n");
            while (getchar() != '\n'); // Clear buffer
            continue;
        }
        
        switch (choice) {
            case 1:
                addRecord();
                break;
            case 2:
                viewRecords();
                break;
            case 3:
                printf("Exiting system. Goodbye!\n");
                break;
            default:
                printf("Invalid option. Please try again.\n");
        }
    } while (choice != 3);

    return 0;
}