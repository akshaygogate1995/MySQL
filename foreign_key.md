-- Create the database
CREATE DATABASE foreignkey;

-- Use the database
USE foreignkey;

-- Create the students table
CREATE TABLE students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    student_fname VARCHAR(30) NOT NULL,
    student_lname VARCHAR(30) NOT NULL,
    student_mname VARCHAR(30),
    student_email VARCHAR(30) NOT NULL UNIQUE KEY,
    student_phone VARCHAR(15) NOT NULL,
    student_alternate_phone VARCHAR(15),
    enrollment_date TIMESTAMP NOT NULL,
    years_of_exp INT NOT NULL,
    student_company VARCHAR(30),
    batch_date VARCHAR(30) NOT NULL,
    source_of_joining VARCHAR(30) NOT NULL,
    location VARCHAR(30) NOT NULL
);
