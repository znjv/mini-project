Done a mini-project on student-course-management-system using My SQL Workbench8.0 CE  with a basic problems

Mini Project: Student Course Management System

This project manages:

Students

Courses

Instructors

Enrollments (students joining courses)

It uses foreign keys, joins, constraints, and practical tasks.

🧱 Step 1 — Create Database
CREATE DATABASE student_management;
USE student_management;

🧱 Step 2 — Create Tables
1️⃣ Students Table
CREATE TABLE students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    gender CHAR(1),
    city VARCHAR(50)
);

2️⃣ Instructors Table
CREATE TABLE instructors (
    instructor_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    department VARCHAR(50)
);

3️⃣ Courses Table
CREATE TABLE courses (
    course_id INT AUTO_INCREMENT PRIMARY KEY,
    course_name VARCHAR(100),
    instructor_id INT,
    credits INT,

    FOREIGN KEY (instructor_id) REFERENCES instructors(instructor_id)
);

4️⃣ Enrollments Table (References Students + Courses)
CREATE TABLE enrollments (
    enrollment_id INT AUTO_INCREMENT PRIMARY KEY,
    student_id INT,
    course_id INT,
    enroll_date DATE,

    FOREIGN KEY (student_id) REFERENCES students(student_id),
    FOREIGN KEY (course_id) REFERENCES courses(course_id)
);

🧩 Step 3 — Insert Sample Data
Students
INSERT INTO students (name, age, gender, city) VALUES
('Arun', 20, 'M', 'Chennai'),
('Divya', 21, 'F', 'Mumbai'),
('Karthik', 22, 'M', 'Bangalore'),
('Sneha', 19, 'F', 'Hyderabad');

Instructors
INSERT INTO instructors (name, department) VALUES
('Dr. Mehta', 'Computer Science'),
('Dr. Priya', 'Mathematics'),
('Dr. Shah', 'Physics');

Courses
INSERT INTO courses (course_name, instructor_id, credits) VALUES
('Database Systems', 1, 4),
('Calculus II', 2, 3),
('Quantum Physics', 3, 4),
('Algorithms', 1, 3);

Enrollments
INSERT INTO enrollments (student_id, course_id, enroll_date) VALUES
(1, 1, '2025-01-05'),
(2, 1, '2025-01-07'),
(3, 2, '2025-01-08'),
(1, 4, '2025-01-10'),
(4, 3, '2025-01-12');

Basic Tasks

View all students.

List all courses with their instructors.

Show all enrollments with student and course names.

Find all students from Chennai.

Count how many students each course has.

Find the average age of students.

List students enrolled in the course “Database Systems”.

Intermediate Tasks

Find all courses taught by Dr. Mehta.

Show students enrolled after 2025-01-07.

Show each instructor and the number of courses they teach.

Update & Delete Tasks

Update the city of “Divya” to “Delhi”.

Increase credits of all Computer Science courses by 1.

Delete all enrollments of the course “Quantum Physics”.

Advanced Tasks

Show students enrolled in more than one course.

Show instructors whose courses have more than 2 students.

🔵 Additional 20 Tasks (Only Tasks)

Show all students along with the courses they are enrolled in (including those not enrolled).

List all instructors and the courses they teach (including those who teach none).

Find the youngest student.

Find the oldest student.

Show all courses with more than 3 credits.

Count how many students are from each city.

List all instructors whose name starts with “D”.

Show all courses that have no students enrolled.

Display names of students who have not enrolled in any course.

Show students who enrolled in January 2025.

Show all courses with their instructor’s department.

Find the number of students enrolled under each instructor.

Get all students whose name contains the letter “a” (case-insensitive).

Show course names sorted alphabetically from A–Z.

Show the top 2 instructors teaching the most courses.

Find all students who enrolled in two or more courses.

Show the total number of enrollments done on each date.

Update all students from Bangalore to “Bengaluru”.

Delete all students who are under 20 years old.

Change the course name “Algorithms” to “Advanced Algorithms”.

List students along with their age and the courses they are enrolled in.

Show instructors who do not teach any course.

Show the total number of courses available in the system.

Find the course with the highest number of credits.

Find the course with the lowest number of credits.

Show all students whose city name ends with the letter “i”.

Show the students who enrolled on weekends (Saturday or Sunday).

Display the latest (most recent) enrollment made.

Display the earliest enrollment made.

Count how many female students are enrolled in any course.

List all courses with the number of students enrolled, sorted from highest to lowest.

Show the instructor who teaches the course with the highest credits.

Find courses where more than one student enrolled on the same date.

Show students who enrolled in courses taught by instructors from the Computer Science department.

Show all instructors and how many total students are enrolled in all their courses combined.

Display the number of enrollments in each month of the year.

List students who live in the same city as their instructor’s department location (assume department = city for comparison).

Show students whose names appear more than once (duplicate names).

Display the list of instructors sorted by department name.

Show all students who are older than the instructor teaching their 
