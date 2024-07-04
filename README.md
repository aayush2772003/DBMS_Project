# DBMS Project - Property Rental Agency

## Overview
This project implements a database system for a Property Rental Agency (PRA), facilitating transactions between property owners and tenants across various cities in India. The system is designed with robust database management features including schema design, data integrity, and manipulation using PostgreSQL.

## Focus
The primary focus of this project includes:
- ER/EER Modeling
- Relational schema design and refinement (Normalization)
- Implementing database with constraints and initial data insertion
- Writing SQL and PL-SQL code for data entry, updates, generating reports, and enforcing complex constraints

## Domain Description
In this database, the following roles are defined:
- **DBA (Database Administrator)**: A super user responsible for user management.
- **Managers**: Manage property records including add, modify, and delete operations.
- **Owners and Tenants**: Users who can either list their properties or rent others' properties.

Properties are categorized as either residential (e.g., independent houses, flats) or commercial (e.g., shops, warehouses).

## Functionality
1. **User Management**: Add users with necessary privileges (DBA).
2. **Property Management**: Add, delete, and update property records (DBA, Managers, Owners).
3. **Rental Management**: Handle rental agreements and maintain rental history.
4. **Reporting**: Generate reports on property rent history and list available properties.

## Schema and Sample SQL Statements
### User Table Creation
```sql
CREATE TABLE "User" (
    AADHARID INT PRIMARY KEY,
    NAME VARCHAR(50) NOT NULL,
    AGE INT NOT NULL,
    DOORNO VARCHAR(20) NOT NULL,
    STREET VARCHAR(50) NOT NULL,
    CITY VARCHAR(20) NOT NULL,
    STATE VARCHAR(20) NOT NULL,
    PINCODE INT NOT NULL,
    LOGINID VARCHAR(20) UNIQUE NOT NULL,
    PASSWORD VARCHAR(20) NOT NULL
);
