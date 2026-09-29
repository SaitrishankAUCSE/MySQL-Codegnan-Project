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

## 🔗 Database Relationships

```text
                 ┌──────────────────┐
                 │    CUSTOMERS     │
                 │ customer_id (PK) │
                 └────────┬─────────┘
                          │
                         1│
                          │N
                 ┌────────▼─────────┐
                 │     BOOKINGS     │
                 │ booking_id (PK)  │
                 │ customer_id (FK) │
                 │ movie_id (FK)    │
                 │ theatre_id (FK)  │
                 └───┬────────┬─────┘
                     │        │
                    N│        │N
                     │        │
              ┌──────▼───┐ ┌──▼────────────┐
              │  MOVIES  │ │   THEATRES    │
              │movie_id  │ │ theatre_id    │
              │   (PK)   │ │     (PK)      │
              └──────────┘ └───────────────┘
```

### Primary Relationships

1. `bookings.customer_id` → `customers.customer_id`
2. `bookings.movie_id` → `movies.movie_id`
3. `bookings.theatre_id` → `theatres.theatre_id`

Each customer, movie, and theatre can be associated with multiple bookings.

---

## 🛠️ Technologies Used

- **Database:** MySQL
- **Language:** SQL
- **Tools:** MySQL Workbench / MySQL CLI
- **Database Type:** Relational Database

---

## 📊 SQL Analysis

The SQL practice is divided into three levels.

### 🟢 Simple Queries

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

### 🟡 Medium Queries

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

### 🔴 Hard Queries

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
└── ER-Diagram.svg
```

`movie_booking.sql` is retained as the complete database dump/backup.

The additional files organize the project for easier learning, execution, and interview review.

---

## 🚀 How to Run the Project

### Step 1 — Install MySQL

Install MySQL Server and optionally MySQL Workbench.

### Step 2 — Open MySQL

Open MySQL Workbench or MySQL CLI.

### Step 3 — Create / select the database

```sql
CREATE DATABASE movie_booking_db;
USE movie_booking_db;
```

### Step 4 — Create and populate the tables

Run the SQL statements from:

```text
Database_Creation_Insertion.txt
```

Alternatively, restore the complete database using:

```text
movie_booking.sql
```

### Step 5 — Verify the tables

```sql
USE movie_booking_db;

SHOW TABLES;
```

Expected tables:

```text
bookings
customers
movies
theatres
```

### Step 6 — View the data

```sql
SELECT * FROM customers;
SELECT * FROM movies;
SELECT * FROM theatres;
SELECT * FROM bookings;
```

### Step 7 — Run the SQL analysis

Execute the queries progressively:

```text
Simple → Medium → Hard
```

---

## 🎓 Learning Outcomes

This project provides practice with:

- Relational database design
- Primary Keys
- Foreign Keys
- One-to-many relationships
- CRUD operations
- Constraints
- Filtering
- Sorting
- Aggregate functions
- JOINs
- GROUP BY
- HAVING
- Subqueries
- CTEs
- Window functions
- SQL-based business analysis

---

## 🔮 Possible Future Improvements

The database can be extended with:

- Seat-level booking management
- Movie show schedules
- Individual theatre screens
- Ticket pricing by seat type
- Offers and discounts
- Cancellation/refund tracking
- Reviews and ratings
- Food and beverage orders
- Online payment transactions
- Theatre-wise occupancy analysis

---

## 👨‍💻 Project Summary

The Movie Ticket Booking System is a practical MySQL project that models customers, movies, theatres, and bookings in a connected relational database.

It progresses from basic SQL operations to multi-table analysis and advanced SQL techniques, making it useful for SQL practice, database learning, and technical interview preparation.

---

## ⭐ Skills Demonstrated

**MySQL · SQL · Database Design · Primary Keys · Foreign Keys · Joins · Aggregation · Subqueries · CTEs · Window Functions · Relational Database Management**
