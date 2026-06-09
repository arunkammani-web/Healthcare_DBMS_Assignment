# Healthcare Appointment and Patient Records System

A relational database project designed and implemented in MySQL to model a healthcare appointment and patient records environment.

This project demonstrates the design of a structured healthcare database for managing patients, doctors, appointments, treatments, and healthcare facilities. It showcases relational modelling, normalization, and SQL-based analysis in a realistic operational setting.

## Problem statement

Healthcare systems manage large volumes of interconnected data across patients, clinicians, appointments, treatments, and facilities. Without a well-designed relational database, this information can become redundant, inconsistent, and difficult to query efficiently.

This project addresses that challenge by building a normalized healthcare database that supports accurate record management, enforces referential integrity, and enables meaningful reporting through SQL.

## Project objectives

The main objectives of this project are to:

- design a relational database from a real-world healthcare scenario,
- implement entity relationships including one-to-one, one-to-many, and many-to-many relationships,
- apply normalization principles up to Third Normal Form (3NF),
- write SQL queries for reporting and business insight generation,
- use keys, constraints, and indexing to support data integrity and performance.

## Why this project matters

This project reflects key database development skills that are directly relevant to real-world systems:

- relational database design,
- entity-relationship modelling,
- normalization,
- SQL querying and reporting,
- structured thinking around data integrity and system design.

The healthcare domain provides a strong practical use case because it involves multiple linked entities, operational workflows, and reporting requirements.

## Project scope

The system is designed to manage the following core areas:

- patients,
- doctors,
- appointments,
- treatments,
- healthcare facilities.

Together, these entities form a simplified healthcare information system capable of supporting both operational data management and analytical queries.

## Database design

### Main entities

The database includes the following main tables:

- **Patient** – stores patient details,
- **Doctor** – stores doctor information and specialization,
- **Facility** – represents hospitals and clinics,
- **Treatment** – stores treatment details and cost,
- **Appointment** – links patients, doctors, and facilities.

### Junction tables

To support many-to-many relationships, the design includes:

- **Patient_Doctor_Treatment**
- **Appointment_Treatment**

### Relationships implemented

| Relationship | Description |
|-------------|-------------|
| 1:N | One patient can have many appointments |
| 1:N | One doctor can have many appointments |
| 1:N | One facility can host many appointments |
| M:N | Patients and doctors are linked through treatments |
| M:N | Appointments and treatments are linked through a junction table |

## Schema features

Key schema features include:

- primary keys for unique row identification,
- foreign keys for referential integrity,
- composite keys for junction tables,
- constraints such as `NOT NULL` and `UNIQUE`,
- indexing to improve query performance.

Example:

```sql
CREATE INDEX idx_doctor_name ON Doctor(Name);
```

## Sample data

The database includes realistic sample records for testing and demonstration purposes, including:

- 4 patients,
- 4 doctors,
- 3 facilities,
- 4 treatments,
- multiple appointments and treatment mappings.

## SQL analysis and business queries

The project answers several healthcare-related business questions, including:

- listing appointments for a specific patient,
- counting total treatments per doctor,
- identifying doctors treating more than a specified number of patients,
- finding facilities used by a patient,
- displaying patients together with their doctors and treatments,
- identifying the most expensive treatment and the responsible doctor,
- finding patients who visit multiple facilities.

## Advanced SQL features

The project uses several important SQL techniques, including:

- `INNER JOIN` operations across multiple tables,
- `GROUP BY` and `HAVING` for aggregation,
- `CASE` statements for classification,
- subqueries for filtering and analysis.

Example:

```sql
CASE
    WHEN COUNT(at.Treatment_ID) > 10 THEN 'High Activity'
    ELSE 'Low Activity'
END
```

## Normalization

The database design follows standard normalization principles:

- **First Normal Form (1NF)** – atomic values and no repeating groups,
- **Second Normal Form (2NF)** – removal of partial dependencies,
- **Third Normal Form (3NF)** – removal of transitive dependencies.

These steps help reduce redundancy, improve data integrity, and support efficient storage and maintenance.

## Technologies used

- **MySQL** – database creation and query execution,
- **SQL** – data definition, manipulation, and reporting,
- **GitHub** – version control and project hosting.

## How to run the project

1. Clone the repository.
2. Open MySQL Workbench, or any compatible SQL environment.
3. Create the database:

```sql
CREATE DATABASE healthcare;
USE healthcare;
```

4. Execute the SQL script containing:
- table creation statements,
- constraints and relationships,
- sample data inserts,
- analytical queries.

## Repository contents

A typical repository structure for this project may include:

```text
.
├── README.md
├── LICENSE
├── healthcare_schema.sql
├── queries.sql
└── docs/
```

## Author

**Kammani Arunsai**  
BSc Computer Science and Digitisation
