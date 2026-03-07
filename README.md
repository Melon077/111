# README.md

A simple and lightweight campus item borrowing management system implemented in Python 

## :book: Contents

- [Introduction]（#introduction）
  
- [Features]

- [Quick Start]

- [Code Structure]

- [Usage Guide]

- [Notes]

- [Submission Info]

<a id="introduction"></a>
## :pencil: Introduction

This project is a **Campus Item Borrowing Management System** developed with pure Python, based on Object-Oriented Programming (OOP) paradigm. It is designed to solve the real-life problem of managing the borrowing and returning of daily items (such as power banks, umbrellas, stationery) on university campuses. The system meets all Task 1 requirements, including using all OOP concepts taught in Week 3 and being split into no less than 3 modules.

## :sparkles: Features

- 📋 **View all items**: Check the ID, name, category and borrowing status of all campus items

- 🔌 **Borrow items**: Verify user and item validity, and record all borrowing operations

- 📥**Return items**: Confirm the lending status of items and complete the return process

- 📜 **View operation records**: Track all borrowing and returning history

- 👤 **User differentiation**: Support basic distinction between ordinary users and administrators (extensible)

## :rocket: Quick Start

### Prerequisites

- Python 3.7+ (No additional third-party libraries required, pure standard library)

### Run the System

1. Clone or download all project files to the same directory. The file structure is as follows:
            `├── user.py          # User/Admin class definition (OOP: Inheritance & Polymorphism)
├── item.py          # Item class definition (OOP: Encapsulation)
├── borrow_system.py # Core borrowing system logic (OOP: Integration)
└── main.py          # Entry point of the system (interactive interface)`

2. Execute the main program in the terminal:
            `python main.py`

## :file_folder: Code Structure

|File Name|Description|
|---|---|
|`user.py`|Defines `User` base class and `Admin` subclass, implements user ID/name management and admin identification (OOP: Inheritance, Polymorphism)|
|`item.py`|Defines `Item` class, manages item attributes (ID/name/category) and borrowing status (OOP: Encapsulation)|
|`borrow_system.py`|Defines `BorrowSystem` core class, integrates items/users/records management, and implements borrow/return business logic (OOP: Integration)|
|`main.py`|System entry point, provides interactive command-line interface for user operations|
## :guide_dog: Usage Guide

After running `main.py`, you will see the interactive menu:

```plain text
===== Campus Item Borrowing Management System =====
1. View all items
2. Borrow an item
3. Return an item
4. View records
0. Exit
Please enter your choice:
```

### 1. View all items

Enter `1` to view all items and their status (example output):

```plain text
ID: I001 | Power Bank | Electronics | status:Can be borrowed
ID: I002 | Umbrella | Daily Necessities | status:Borrowed
```

### 2. Borrow an item

Enter `2`, then input your **User ID** and **Item ID** in turn:
        
- Success case: Enter `S001` (user ID) and `I001` (item ID) → `Borrowing Successfully`
        
- Failure case: Non-existent user/item → `User/Item doesn't exist`; Item already borrowed → `Item has been borrowed`

### 3. Return an item

Enter `3`, then input the **Item ID** to return:

- Success case: Return a lent-out item → `Return Successfully`
- Failure case: Non-existent item → `Item doesn't exist`; Item not lent out → `Item was not lent out`

### 4. View records

Enter `4` to check all borrowing/returning operation records (example output):

```plain text
S001 borrow I001
I001 Item returned
```

### 0. Exit

Enter `0` to exit the system → `Exiting system`

## :warning: Notes

- The system uses in-memory storage (no persistent database), all data will be lost after exiting the program.

- Admin users currently only differ from ordinary users in the `is_admin()` method return value, and can be extended with admin-only functions (e.g., add/delete items) as needed.

- User/Item ID is case-sensitive (e.g., `S001` ≠ `s001`), please enter according to the test data or custom rules.

- This project uses all OOP concepts taught in Week 3 and meets the minimum requirement of 3 modules.

## :clipboard: Submission Info

- Course: COMP2090SEF 
- Project Task: Task 1 (OOP Application Development)

- GitHub Repository: [Add your repository link here]

- Team Members (COMP2090SEF): [Name 1 (Student ID), Name 2 (Student ID), Name 3 (Student ID)]


