Library Management System – Book Issue and Return

1. Problem Statement

The Library Management System – Book Issue and Return is designed to manage student details, book details, book issuing, book returning, and due dates.

The system checks the availability of a book before issuing it to a student. It records the issue date and due date. When the book is returned, the system records the return date, checks whether it was returned on time, and updates the book status to Available.

---

2. Student Details

Field| Details
Student Name| Spoorti Patil
Roll Number| U15CZ26S0080
Class| BCA 1ST YEAR 'B'

---

3. Feature Set

1. Student Details
2. Book Details
3. Book Issue
4. Book Return
5. Due Date
6. Return Status
7. Book Availability Status

---

4. Requirements

4.1 Algorithm Requirements

The algorithm should:

1. Start the Library Management System.
2. Enter and store student details:
   - Student ID
   - Student Name
   - Contact Number
   - Department
3. Enter and store book details:
   - Book ID
   - Book Name
   - Author Name
   - Book Status
4. Check whether the selected book is available.
5. If the book is available:
   - Issue the book to the student.
   - Update the book status to Issued.
   - Store the issue details.
   - Assign and store the due date.
6. When the student returns the book:
   - Record the return details.
   - Record the return date.
7. Compare the return date with the due date.
8. Display the appropriate return status.
9. Update the book status to Available.
10. End the Library Management System.

---

4.2 Flowchart Requirements

The flowchart should include:

- Oval – Start/End
- Parallelogram – Input/Output
- Rectangle – Process
- Diamond – Decision
- Arrows – Flow direction

Flowchart Process

Start

↓

Enter Student Details

↓

Enter Book Details

↓

Check Book Availability

↓

Is Book Available?

YES

↓

Issue Book

↓

Update Book Status = Issued

↓

Store Issue Details

↓

Assign Due Date

↓

Return Book

↓

Record Return Date

↓

Check Return Date with Due Date

↓

Display Return Status

↓

Update Book Status = Available

↓

End

NO

↓

Display "Book Not Available"

↓

End

The flowchart should clearly show both YES and NO paths from the book availability decision.

---

5. ER Diagram Requirements

The system contains three main entities:

5.1 STUDENT

Attribute| Description
Student_ID| Primary Key (PK)
Student_Name| Name of the student
Contact_Number| Contact number
Department| Student's department

STUDENT Entity

STUDENT
-------------------------
PK Student_ID
   Student_Name
   Contact_Number
   Department

---

5.2 BOOK

Attribute| Description
Book_ID| Primary Key (PK)
Book_Name| Name of the book
Author_Name| Name of the author
Book_Status| Available / Issued

BOOK Entity

BOOK
-------------------------
PK Book_ID
   Book_Name
   Author_Name
   Book_Status

---

5.3 ISSUE_RETURN

Attribute| Description
Issue_Return_ID| Primary Key (PK)
Student_ID| Foreign Key (FK)
Book_ID| Foreign Key (FK)
Issue_Date| Date on which book is issued
Due_Date| Last date for returning the book
Return_Date| Date on which book is returned
Return_Status| On Time / Late

ISSUE_RETURN Entity

ISSUE_RETURN
-------------------------
PK Issue_Return_ID
FK Student_ID
FK Book_ID
   Issue_Date
   Due_Date
   Return_Date
   Return_Status

---

6. ER Diagram Relationships

The relationships are:

STUDENT  1 -------- N  ISSUE_RETURN  N -------- 1  BOOK

Relationship Explanation

- One STUDENT can have multiple issue/return records.
- One BOOK can appear in multiple issue/return records over time.
- ISSUE_RETURN connects STUDENT and BOOK.
- ISSUE_RETURN stores issue date, due date, return date, and return status.
- "Student_ID" in ISSUE_RETURN is a Foreign Key referencing STUDENT.
- "Book_ID" in ISSUE_RETURN is a Foreign Key referencing BOOK.

---

7. Overall System Flow

START
  |
  v
Enter Student Details
  |
  v
Enter Book Details
  |
  v
Check Book Availability
  |
  v
Is Book Available?
 /              \
YES              NO
 |                |
 v                v
Issue Book    Display "Book
 |             Not Available"
 v                |
Update Status     v
"Issued"         END
 |
 v
Store Issue Details
 |
 v
Assign Due Date
 |
 v
Return Book
 |
 v
Record Return Date
 |
 v
Check Due Date
 |
 v
Display Return Status
 |
 v
Update Status
"Available"
 |
 v
END

---

8. Database Design Summary

Entity| Primary Key| Important Attributes
STUDENT| Student_ID| Student_Name, Contact_Number, Department
BOOK| Book_ID| Book_Name, Author_Name, Book_Status
ISSUE_RETURN| Issue_Return_ID| Student_ID, Book_ID, Issue_Date, Due_Date, Return_Date, Return_Status

---

9. Expected Output

The system should be able to:

- Store student information.
- Store book information.
- Check book availability.
- Issue an available book.
- Change book status to Issued.
- Store issue and due-date information.
- Record returned books.
- Compare the return date with the due date.
- Display the return status.
- Change the returned book status to Available.

---

10. Conclusion

The Library Management System – Book Issue and Return provides a simple method for managing library books and student records. It helps track issued books, due dates, return dates, and book availability. The algorithm, flowchart, and ER diagram provide a clear representation of how the system works and are suitable for a 1st-year BCA assignment.
