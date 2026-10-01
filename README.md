# 🎬 Movie Ticket Booking System — MySQL SQL Project

A MySQL-based relational database project for managing customers, movies, theatres, and movie ticket bookings.

The project demonstrates practical SQL and relational database concepts including database design, primary keys, foreign keys, constraints, CRUD operations, filtering, sorting, aggregate functions, JOINs, GROUP BY, HAVING, subqueries, CTEs, and window functions.

---

## 📌 Project Overview

The Movie Ticket Booking System models a basic movie-ticket booking workflow using a relational database.

The database contains four main entities:

- 👤 Customers
- 🎬 Movies
- 🏢 Theatres
- 🎟️ Bookings

The `bookings` table connects customers, movies, and theatres through foreign-key relationships.

---

## 🎯 Objectives

This project focuses on:

- Designing a relational database using MySQL
- Creating related tables
- Applying Primary Key and Foreign Key relationships
- Maintaining referential integrity
- Storing customer, movie, theatre, and booking information
- Practicing SQL filtering and sorting
- Performing aggregate analysis
- Using JOINs across multiple tables
- Using GROUP BY and HAVING
- Writing subqueries
- Practicing CTEs and window functions
- Answering practical movie-booking business questions

---

## 🗄️ Database Structure

**Database:** `movie_booking_db`

| Table | Purpose |
|---|---|
| `customers` | Stores customer information |
| `movies` | Stores movie information |
| `theatres` | Stores theatre information |
| `bookings` | Stores ticket booking information |

### Customers

| Column | Description |
|---|---|
| `customer_id` | Unique customer identifier |
| `customer_name` | Customer name |
| `gender` | Customer gender |
| `city` | Customer city |
| `signup_date` | Customer signup date |

### Movies

| Column | Description |
|---|---|
| `movie_id` | Unique movie identifier |
| `movie_name` | Movie name |
| `genre` | Movie genre |
| `language` | Movie language |
| `duration_minutes` | Movie duration in minutes |

### Theatres

| Column | Description |
|---|---|
| `theatre_id` | Unique theatre identifier |
| `theatre_name` | Theatre name |
| `city` | Theatre city |
| `total_seats` | Total theatre seats |

### Bookings

| Column | Description |
|---|---|
| `booking_id` | Unique booking identifier |
| `customer_id` | Customer reference |
| `movie_id` | Movie reference |
| `theatre_id` | Theatre reference |
| `show_date` | Movie show date and time |
| `seats_booked` | Number of seats booked |
| `ticket_amount` | Booking amount |
| `booking_status` | Booking status |
| `payment_method` | Payment method |

---

## 🔗 ER Diagram & Database Relationships

The following ER diagram represents the complete database design of the Movie Ticket Booking System, including entities, attributes, primary keys, foreign keys, relationships, and cardinality.

<p align="center">
  <img src="ER-Diagram.png" alt="Movie Ticket Booking System ER Diagram" width="100%">
</p>

### Primary Relationships

| Relationship | Cardinality | Description |
|---|---|---|
| Customers → Bookings | 1 : N | One customer can make multiple bookings |
| Movies → Bookings | 1 : N | One movie can have multiple bookings |
| Theatres → Bookings | 1 : N | One theatre can have multiple bookings |

### Foreign Key Relationships

- `bookings.customer_id` → `customers.customer_id`
- `bookings.movie_id` → `movies.movie_id`
- `bookings.theatre_id` → `theatres.theatre_id`

Primary keys uniquely identify records, while foreign keys maintain relationships between the related tables and help preserve referential integrity.

---

## 🛠️ Technologies Used

- **Database:** MySQL
- **Language:** SQL
- **Tools:** MySQL Workbench / MySQL CLI
- **Version Control:** Git / GitHub
- **Database Type:** Relational Database

---

## 📊 SQL Analysis

The SQL practice is divided into three levels containing a total of **60 SQL queries**.

### 🟢 Simple Queries — 20

Basic SQL operations:

- SELECT
- WHERE
- LIKE
- BETWEEN
- ORDER BY
- LIMIT
- DISTINCT
- COUNT()
- SUM()
- AVG()
- MIN()
- MAX()
- String functions
- Date functions

### 🟡 Medium Queries — 20

Intermediate relational analysis:

- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- CROSS JOIN
- GROUP BY
- HAVING
- Aggregate functions
- CASE
- Subqueries
- Multi-table analysis

### 🔴 Hard Queries — 20

Advanced SQL analysis:

- Nested subqueries
- Correlated subqueries
- CTEs
- Window functions
- RANK()
- DENSE_RANK()
- ROW_NUMBER()
- PARTITION BY
- Complex aggregations
- Business-oriented analysis

### Query Distribution

| Level | Number of Queries |
|---|---:|
| 🟢 Simple | 20 |
| 🟡 Medium | 20 |
| 🔴 Hard | 20 |
| **Total** | **60** |

---

## 💼 Business Questions Answered

The project can be used to answer questions such as:

- Which movies have the most bookings?
- Which customers have made the most bookings?
- Which theatres receive the most bookings?
- What is the total ticket revenue?
- What is the average booking amount?
- Which movie generates the highest ticket revenue?
- Which city has the most customers?
- Which payment method is used most frequently?
- How many seats have been booked for each movie?
- Which theatres have the highest booking activity?
- Which customers have never made a booking?
- Which movies have no bookings?
- What is the average number of seats per booking?
- What are the highest-value bookings?
- How does booking activity vary by date?

---

## 📁 Repository Structure

```text
MySQL-Codegnan-Project/
│
├── README.md
├── movie_booking.sql
│
├── Database_Creation_Insertion.txt
├── Execution.txt
├── Simple_queries.txt
├── Medium_queries.txt
├── Hard_queries.txt
│
└── ER-Diagram.png