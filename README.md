Imports the datetime class to fetch and format the current date when attendance is marked.
#class Student:
Defines a class to represent an individual student.
#def __init__(self, roll_no, name):
Constructor that initializes a student object.
#self.roll_no = roll_no
Stores the student’s roll number.
#self.name = name
Stores the student’s name.
#class AttendanceSystem:
Main class that manages students and attendance records.
#def __init__(self):
Initializes the attendance system
#self.students = {}
Dictionary to store student objects using roll number as key.
#self.attendance = {}
Dictionary to store attend        print("Student added successfully!\n")
ance records.
#def add_student(self):
Adds a new student to the system
#roll = input("Enter Roll Number: ")
Takes roll number as input.
#name = input("Enter Student Name: ")
Takes student name as input
#if roll in self.students:
Checks if the student already exists.
#print("Student already exists!\n")
#return
Stops execution if duplicate roll number is found.
#self.students[roll] = Student(roll, name)
Creates a Student object and stores it in the dictionary.
#print("Student added successfully!\n")
Confirms successful student addition.
#def view_students(self):
Displays all registered students.
#if not self.students:
Checks if there are no students
#print("No students found.\n")
#return
Displays message and exits method.
#print("\nRoll No | Name")
#print("-" * 20)
Prints table header.
#for s in self.students.values():
Iterates through all student objects.
#print(f"{s.roll_no} | {s.name}")
Displays roll number and name.
#def mark_attendance(self):
Marks attendance for all students on the current date.
#if not self.students:
Ensures students exist before marking attendance.
#print("No students available. Add students first.\n")
#return
Prevents attendance marking if student list is empty.
#date = datetime.now().strftime("%d-%m-%Y")
Fetches today’s date in DD-MM-YYYY format.
#self.attendance[date] = {}
Creates an attendance record for the current date.
#print(f"\nMarking attendance for {date}")
Displays attendance date.
#for roll, student in self.students.items():
Iterates through each student.
#while True:
Loop to ensure valid attendance input.
#status = input(f"{student.name} (P/A): ").upper()
Accepts attendance input and converts it to uppercase.
#if status in ("P", "A"):
Validates input.
#self.attendance[date][roll] = status
 break
Stores attendance and exits loop.
#else:
  print("Enter only P or A")
Prompts again for invalid input.
#print("Attendance marked successfully!\n")
Confirms attendance marking.
#def view_attendance(self):
Displays all attendance records.
#if not self.attendance:
Checks if attendance records exist.
#print("No attendance records found.\n")
 return
Displays message if no records found.
#for date, records in self.attendance.items():
Iterates through each date
#name = self.students[roll].name
Fetches student name using roll number.
#print(f"{roll} | {name} | {status}")
Displays attendance details.
# def menu(self):
Displays menu and handles user interaction.
#while True:
Runs continuously until exit option is chosen.
#print("===== Attendance Management System =====")
Displays system title.
#print("1. Add Student")
print("2. View Students")
print("3. Mark Attendance")
print("4. View Attendance")
print("5. Exit")
Menu options.
#choice = input("Enter your choice: ")
Accepts user choice.
#if choice == "1":
self.add_student()
Calls add student method.
#elif choice == "2":
self.view_students()
Calls view students method.
#elif choice == "3":
self.mark_attendance()
Calls mark attendance method.
#elif choice == "4":
self.view_attendance()
Calls view attendance method.
#elif choice == "5":
print("Exiting system.")
break
Exits the program.
#else:
print("Invalid choice. Try again.\n")
Handles invalid menu input.
system = AttendanceSystem()
Creates an object of AttendanceSystem.
system.menu()
Starts the menu-driven application.

