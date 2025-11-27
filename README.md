# Student Record Management (C Project)

This is a simple **Student Record Management System** written in C.  
It demonstrates how to use **structures**, **arrays**, and **functions** to store and manage basic student details.

---

## 🎯 Objective

To create a console-based program that allows the user to:

- Add student records
- View all stored student records
- Exit the program safely

---

## 🧾 Features

- Stores details for up to **10 students**
- Each student record includes:
  - `Roll Number` (integer)
  - `Name` (string)
  - `Marks` (float, out of 100)
- Validates user input for:
  - Roll number (must be a valid integer)
  - Marks (must be a valid floating-point number)
- Shows a **menu-driven interface**:
  1. Add Record  
  2. View All Records  
  3. Exit  

---

## 🧱 Program Structure

### 1. `struct Student`

A custom data type to store student information:

 ![Image Alt](https://github.com/barun0045/details.c-project/blob/569fd2edc7fe1f24b6998c7e5b54d68aaa42440b/Screenshot%202025-11-24%20192310.png)
![Image Alt](https://github.com/barun0045/details.c-project/blob/f97b14672990b67c5804da82eb5963f83d8aaada/Screenshot%202025-11-24%20192357.png)
 ![Image Alt](https://github.com/barun0045/details.c-project/blob/f97b14672990b67c5804da82eb5963f83d8aaada/Screenshot%202025-11-24%20192411.png)
 ![Image Alt](https://github.com/barun0045/details.c-project/blob/f97b14672990b67c5804da82eb5963f83d8aaada/Screenshot%202025-11-24%20192425.png)
```c
struct Student {
    int rollNumber;
    char name[50];
    float marks;
};




