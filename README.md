# 🎬 Movie Ticket Booking System — MySQL

A relational database project built using **MySQL** to manage customers, movies, theatres, and movie ticket bookings.

This project demonstrates practical SQL and relational database concepts including **DDL, DML, primary keys, foreign keys, constraints, JOINs, aggregate functions, GROUP BY, HAVING, subqueries, and data retrieval**.

---

## 📌 Project Overview

The Movie Ticket Booking System is designed to manage the core data involved in a movie booking workflow.

The database contains four main entities:

- 👤 Customers
- 🎬 Movies
- 🏢 Theatres
- 🎟️ Bookings

The tables are connected using primary keys and foreign keys to maintain relationships between the data.

---

## 🗄️ Database Structure

### Customers

Stores customer information.

| Column | Description |
|---|---|
| customer_id | Unique customer identifier |
| name | Customer name |
| phone | Customer phone number |
| email | Customer email |

### Movies

Stores movie-related information.

| Column | Description |
|---|---|
| movie_id | Unique movie identifier |
| title | Movie title |
| genre | Movie genre |
| duration | Movie duration |
| language | Movie language |

### Theatres

Stores theatre information.

| Column | Description |
|---|---|
| theatre_id | Unique theatre identifier |
| theatre_name | Theatre name |
| location | Theatre location |

### Bookings

Stores movie ticket booking information.

| Column | Description |
|---|---|
| booking_id | Unique booking identifier |
| customer_id | Customer reference |
| movie_id | Movie reference |
| theatre_id | Theatre reference |
| booking_date | Date of booking |
| seats | Number of seats |
| total_amount | Total booking amount |

---

## 🔗 Relationships

```text
Customers
    │
    │ customer_id
    ▼
Bookings
    │
    ├──────────────► Movies
    │
    └──────────────► Theatres
