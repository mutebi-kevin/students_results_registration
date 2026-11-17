
STUDENT RESULTS REGISTER
C++17 PROJECT README

1. PROJECT OVERVIEW

The Student Results Register is a console-based application developed in C++17. It is designed to store, manage, search and sort student academic records.

The application uses a custom Dynamic Array to store student records. It also demonstrates searching and sorting algorithms, file handling, and basic memory management.

2. PROJECT OBJECTIVES

The main objectives are to:
- Store student records containing a student ID, name, course and marks.
- Add and manage records using a custom Dynamic Array.
- Load student records from a text file.
- Save student records to a text file.
- Search for student records.
- Sort student records using the implemented sorting algorithms.
- Demonstrate safe handling of invalid array positions and other errors.

3. PROJECT STRUCTURE

STUDENT RESULTS REGISTRATION
|--main.cpp
|--Students.txt
|--README.txt


File descriptions:

- main.cpp: Contains  all  the main program flow and user interaction.
-students.txt: Contains the 10 student records loaded by the application.
- README.txt: Provides project information and instructions.

4. STUDENT DATA FORMAT

The input file stores one student per line. Each line contains four comma-separated fields in this order:

StudentID,StudentName,Course,Marks

Example:
1001,Kevin Mutebi,Computer Science,85
1002,Reagan Mubiru,Information Technology,72
1003,James Ssemusu,Software Engineering,90

The marks are numeric values. The application calculates the grade from the marks if grade calculation is implemented in Student.h or the relevant program logic.

Important: The file path used by the file-loading code must match the location of the file. With the folder structure above, the program should load "data/students.txt" when it is run from the project root folder.

5. MAIN FEATURES

- Student record management: stores student IDs, names, courses and marks.
- Dynamic storage: the custom dynamic array can increase its capacity when more records are added.
- File input: reads student records from the text file.
- File output: saves records to a text file when the program's save functionality is used.
- Searching: provides the search methods implemented in Searching.h.
- Sorting: provides the sorting methods implemented in Sorting.h.
- Error handling: checks invalid positions and handles file or input errors where implemented.

6. DATA STRUCTURE

The project uses a custom Dynamic Array rather than relying on std::vector to store the student records.

A dynamic array stores elements in a block of memory. It tracks:
- Size: the number of records currently stored.
- Capacity: the number of records the allocated memory can hold before it must grow.

When the array becomes full, it allocates a larger memory block, copies the existing records into it and releases the old block. This allows the application to accommodate a changing number of student records.

7. ALGORITHMS

The project includes the searching and sorting algorithms implemented in the source files:

Searching:
- Linear Search: checks records one by one until a matching record is found or the records are exhausted.
- Binary Search: repeatedly reduces the search range by half. The data must be sorted using the same search key before Binary Search is used.

Sorting:
- Insertion Sort: builds a sorted section by inserting each next record into its correct position.
- Merge Sort: divides the records into smaller sections, sorts those sections and merges them into one sorted result.

The exact search fields, sort order and function names are determined by the implementations in Searching.h and Sorting.h.

8. REQUIREMENTS

- A C++17-compatible compiler, such as GCC or Clang.
- A terminal or command prompt.
- The project source files and the data/students.txt input file.

9. COMPILING THE PROJECT

Open a terminal in the StudentResultsRegister project root folder and run:

g++ -std=c++17 -Wall -Wextra -I include src/main.cpp -o StudentResultsRegister.exe

This command:
- Selects the C++17 language standard.
- Enables common compiler warnings.
- Tells the compiler where the header files are located.
- Compiles src/main.cpp.
- Creates the executable StudentResultsRegister.exe.

10. RUNNING THE PROJECT

From the same project root folder, run:

.\StudentResultsRegister.exe

If using PowerShell, the command is:

.\StudentResultsRegister.exe

Run the application from the project root folder so that a relative input path such as "data/students.txt" can be found.

11. TESTING CHECKLIST

Before submitting or demonstrating the project, check that:
- The program compiles without errors.
- The input file contains at least the required number of sample records.
- All records load correctly.
- The displayed student details are correct.
- Searching finds an existing student.
- Searching handles a student who does not exist.
- Sorting places records in the expected order.
- Invalid array positions are rejected safely where bounds checking is implemented.
- Saving records creates or updates the expected output file.
- The program handles a missing or inaccessible input file appropriately.

12. LIMITATIONS AND POSSIBLE IMPROVEMENTS

Possible future improvements include:
- A graphical user interface.
- More detailed validation of student IDs and marks.
- Editing and deleting student records through the menu.
- More search and sorting options.
- Exporting reports to CSV or PDF.
- Stronger handling of commas and special characters in names and course titles.

13. CONCLUSION

The Student Results Register demonstrates how a C++ application can manage student records using a custom dynamic array, file handling, searching and sorting algorithms. It also provides practical experience with classes or structures, templates, pointers, dynamic memory allocation and error handling.