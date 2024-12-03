# Week 11

    - Project in  PHP & OOP & MYSQL
---
- Task <br>
    - Upload this project to Github
        - Develop an Online Course Management System

            - Description:
                Build a system that manages courses, instructors, and students, with relationships between them. Each course can have multiple students and one instructor. Students can enroll in multiple courses.

            - Requirements:
                Database Design:
                - Create the following tables:
                    - Users:
                        - Hint use enum for differentiate between students and instructors
                    - Courses
                    - Enrollments
                - Features:
                    - User Authentication:
                        - Login and registration for both instructors and students.
                        - Role-based access control to restrict access to certain pages.
                    - Course Management (Instructors):
                        - Create, edit, and delete courses.
                        - View a list of enrolled students for their courses.
                    - Student Features:
                        - View available courses.
                        - Enroll in a course.
                        - View a list of enrolled courses.
                    - Admin Features (Optional):
                        - View all users, courses, and enrollments.
                        - Delete any user, course, or enrollment.
            - Implementation Details:

                - Use PHP OOP principles:
                    - A Database class for connection handling.
                    - Separate classes for User, Course, and Enrollment with appropriate methods for CRUD operations.
                - Implement prepared statements for database interactions.
                - Use password hashing for secure user authentication.
                - Create relationships between classes to reflect database relationships.
                - Add pagination for course and user lists.
                - Use AJAX for enrollment actions (optional).
            - Extra Challenges (Optional):

                - Implement search and filter options for courses and students.
                - Add email notifications for course enrollment.
                - Provide a dashboard with stats (e.g., total courses, students, and enrollments).
                - Use a modern UI framework like Bootstrap or Tailwind CSS for styling.