# Healthcare_DBMS_Project



This project is my first hands-on database project, where I designed and implemented a Healthcare Appointment and Patient Records System using MySQL.


It showcases my ability to:
Design a relational database from a real-world scenario
Implement entity relationships (1:N and M:N)
Apply normalization techniques (up to 3NF)
Write advanced SQL queries to solve business problems



 Why This Project Matters ?

Although this is my first project, it reflects strong foundational skills in:

Database Design Thinking
Relational Modeling (ER concepts)
SQL Development & Query Optimization
Data Analysis using SQL queries
This project simulates a real healthcare system, making it relevant for real-world applications.


Healthcare Appointment and Patient Records System

 Project Overview

This project is a Healthcare Database Management System developed as part of the Database Design and Implementation module. It demonstrates the design and implementation of a relational database to manage:

Patients
Doctors
Appointments
Treatments
Healthcare Facilities
The system is built using MySQL and focuses on applying database design principles, normalization, and advanced SQL querying.

 Objectives

The main objectives of this project are:
Design a structured relational database from a real-world healthcare scenario
Implement entity relationships (1:1, 1:N, M:N)
Apply normalization techniques (up to 3NF)
Write SQL queries for business insights and reporting
Use constraints, indexing, and aggregation functions



 Database Design
 
Entities Created
The database consists of the following main tables:
Patient – Stores patient details
Doctor – Stores doctor information and specialization
Facility – Represents hospitals/clinics
Treatment – Stores treatment details and cost
Appointment – Links patients, doctors, and facilities
Relationship Tables (Junction Tables)
To handle many-to-many relationships:
Patient_Doctor_Treatment
Appointment_Treatment




  Relationships Implemented
  
Relationship Type	Description
1:N	One patient → many appointments
1:N	One doctor → many appointments
1:N	One facility → many appointments
M:N	Patients ↔ Doctors (via treatments)
M:N	Appointments ↔ Treatments

  
  Technologies Used

MySQL – Database creation and querying
SQL – Data definition and manipulation
GitHub – Version control and project hosting



  Database Schema

Key features of the schema:
Primary Keys for unique identification
Foreign Keys for referential integrity
Composite Keys for junction tables
Constraints (NOT NULL, UNIQUE)
Indexing for performance optimization

Example:

CREATE INDEX idx_doctor_name ON Doctor(Name);

Sample Data

The database includes realistic sample data:

4 Patients
4 Doctors
3 Facilities
4 Treatments

Multiple appointments and treatment mappings

 Business Queries Implemented

The project answers key healthcare-related business questions:
List appointments for a specific patient
Count total treatments per doctor
Identify doctors treating more than a set number of patients
Find facilities used by a patient
Display patients with their doctors and treatments
Identify the most expensive treatment and responsible doctor
Find patients visiting multiple facilities

 Advanced SQL Features

JOIN operations (INNER JOIN across multiple tables)
GROUP BY & HAVING for aggregation
CASE statements for classification
Subqueries for dynamic filtering

Example:

CASE
WHEN COUNT(at.Treatment_ID) > 10 THEN 'High Activity'
ELSE 'Low Activity'
END

 Normalization

The database design follows normalization principles:

1NF – Atomic values, no repeating groups
2NF – Removal of partial dependencies
3NF – Removal of transitive dependencies

This ensures:

Reduced redundancy
Improved data integrity
Efficient data storage

 Key Features

 Fully normalized relational database
 Supports complex healthcare relationships
 Includes realistic sample data
 Optimized with indexing
 Business-driven SQL queries

 How to Run the Project

Clone the repository
Open MySQL Workbench (or any SQL tool)
Run the SQL script:
create database healthcare;
use healthcare
Execute all table creation and insert statements
Run the queries to explore insights

 Assignment Context

This project was developed based on a university assignment requiring:

ER modeling
SQL implementation
Query development
Normalization
Data analysis using SQL 
DBDI-Set Exercise-2

 Author

Kammani Arunsai
BSc Computer Science and Digitisation
