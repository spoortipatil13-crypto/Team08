README - Online Course Enrollment

Problem Statement

(11) COURSE DETAIL - COURSE ENROLLMENT

Feature Set: 03

This project describes a simple Online Course Enrollment system for a
1st-year BCA DBMS assignment. It manages student details, course
details, enrollment, payment, and enrollment status.

Student Details

-   Name: sharada kamble
-   Roll Number: U15CZ26S0060
-   Class: BCA 1st year â€˜Bâ€™

Feature Set

1.  Student Details
2.  Course Details
3.  Enrollment
4.  Payment
5.  Enrollment Status

Objective

The objective of this system is to allow a student to select a course,
create an enrollment, view the course fee, make a payment, and receive
an enrollment status based on the payment result.

Algorithm

1.  Start the process.
2.  Enter and store student details:
    -   Student_ID
    -   Student_Name
    -   Email
    -   Contact_No
3.  Enter and store course details:
    -   Course_ID
    -   Course_Name
    -   Course_Fee
    -   Course_Duration
4.  Allow the student to select a course.
5.  Create an enrollment record.
6.  Check whether the enrollment details are valid.
7.  Display the course fee.
8.  Process the payment.
9.  Check whether the payment is successful.
10. If payment is successful, set Enrollment_Status to Enrolled.
11. If payment is unsuccessful, set Enrollment_Status to Pending/Failed.
12. Display student details, course details, enrollment details, payment
    status, and enrollment status.
13. End the process.

Flowchart Process

    START
      |
      v
    Enter Student Details
      |
      v
    Enter Course Details
      |
      v
    Select Course
      |
      v
    Create Enrollment
      |
      v
    Display Course Fee
      |
      v
    Make Payment
      |
      v
    Is Payment Successful?
      |                    |
     Yes                   No
      |                    |
      v                    v
    Set Status          Set Status
    as Enrolled         as Pending/Failed
      |                    |
      +---------+----------+
                |
                v
    Display Enrollment Details and Status
                |
                v
               END

ER Diagram

1. STUDENT

  Attribute      Type
  -------------- ------------------
  Student_ID     Primary Key (PK)
  Student_Name   Attribute
  Email          Attribute
  Contact_No     Attribute

2. COURSE

  Attribute         Type
  ----------------- ------------------
  Course_ID         Primary Key (PK)
  Course_Name       Attribute
  Course_Fee        Attribute
  Course_Duration   Attribute

3. ENROLLMENT

  Attribute           Type
  ------------------- ------------------
  Enrollment_ID       Primary Key (PK)
  Student_ID          Foreign Key (FK)
  Course_ID           Foreign Key (FK)
  Enrollment_Date     Attribute
  Enrollment_Status   Attribute

4. PAYMENT

  Attribute        Type
  ---------------- ------------------
  Payment_ID       Primary Key (PK)
  Enrollment_ID    Foreign Key (FK)
  Payment_Date     Attribute
  Amount           Attribute
  Payment_Status   Attribute

Relationships and Cardinality

-   STUDENT â†’ ENROLLMENT: One student can have many enrollments (1:N).
-   COURSE â†’ ENROLLMENT: One course can have many enrollments (1:N).
-   ENROLLMENT â†’ PAYMENT: One enrollment can have one payment record
    (1:1) in this assignment model.

ER Diagram Structure

    STUDENT (1) --------< ENROLLMENT >-------- (1) COURSE
                           |
                           |
                          (1)
                           |
                           v
                        PAYMENT

Entity Relationships

    STUDENT
      |
      | 1:N
      v
    ENROLLMENT
      ^
      | N:1
      |
    COURSE

    ENROLLMENT
      |
      | 1:1
      v
    PAYMENT

Standard ER Notation

-   Rectangle = Entity
-   Oval = Attribute
-   Diamond = Relationship
-   PK = Primary Key
-   FK = Foreign Key
-   1:N = One-to-Many
-   1:1 = One-to-One

Requirements Checklist

-   Store student details.
-   Store course details.
-   Allow course selection and enrollment.
-   Validate enrollment details.
-   Display the course fee.
-   Process payment.
-   Check payment success.
-   Set enrollment status to Enrolled or Pending/Failed.
-   Display all relevant details and status.
-   Use only the four required entities: STUDENT, COURSE, ENROLLMENT,
    and PAYMENT.
-   Clearly identify PKs and FKs.
-   Show relationships and cardinalities.
-   Keep the ER diagram simple, neat, and suitable for a 1st-year BCA
    DBMS assignment.

Expected Output

After completing the enrollment process, the system should display:

-   Student details
-   Selected course details
-   Enrollment details
-   Payment amount and payment status
-   Final enrollment status

Conclusion

The Online Course Enrollment system provides a structured way to manage
students, courses, enrollments, and payments. The algorithm explains the
step-by-step process, while the flowchart represents the process
visually and the ER diagram represents the database entities,
attributes, relationships, and cardinalities.

------------------------------------------------------------------------

Student: sharada kamble
Roll Number: U15CZ26S0060
Class: BCA 1st year â€˜Bâ€™
