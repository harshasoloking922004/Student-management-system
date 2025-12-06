Student Management System (C++ – File Handling, Login System, Role-Based Access)

This project is a console-based Student Management System implemented in C++ using
file handling, role-based access control, and a secure password input mechanism (no echo).

It supports three types of users:

Admin – Full access (Add, Display, Search, Update, Delete)

Staff – Limited access (Display, Search)

Guest – View only (Display)

Features
🔐 Login System

Username & password authentication

Password input hidden using termios

Credentials stored in users.txt

👥 User Roles
Role	Access
Admin	Add, Display, Search, Update, Delete
Staff	Display, Search
Guest	Display only
🎓 Student Management

Add a new student

Show all students

Search student by roll number

Update student details

Delete student record

All data stored in students.txt

📁 File Handling

The project uses two files:

users.txt – Stores user credentials

students.txt – Stores student records

If files don’t exist, the program automatically generates default data.

Default Login Credentials

The program auto-creates these if users.txt is missing:

Username	Password	Role
admin	admin123	admin
staff1	staff123	staff
guest	guest	guest
How to Compile & Run
Linux / Mac
g++ main.cpp -o sms
./sms

Windows (MinGW)
g++ main.cpp -o sms.exe
sms.exe

Project Structure
├── main.cpp
├── students.txt     (auto-created)
└── users.txt        (auto-created)

Security Feature

The function getPassword() uses termios to turn off terminal echo, so passwords appear as:

Enter password: ******

Screenshots (Conceptual)
Login
============== LOGIN SCREEN ============
Enter username: admin
Enter password: ******

Admin Menu
=== Admin Menu ===
1. Add new Student
2. Display all Students
3. Search Student
4. Update Student
5. Delete Student
6. Logout

