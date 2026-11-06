# 🗄️ Employee & Reward Database – SQL Project

A MySQL project that creates two related tables, inserts sample data, and practises 25+ SQL queries on strings, dates, sorting, filtering and pattern matching.

## 🎯 Objective
To practise database design (primary key, foreign key, one-to-many relationship) and core SQL query skills on employee and reward data.

## 🛠️ Tools Used
- **MySQL 8.0**
- **MySQL Workbench**

## 🧱 Database Structure
Database: `shabana`

**`employee2`** – 7 employees across Finance, IT, Banking and Insurance
| Column | Type | Notes |
|--------|------|-------|
| employee_id | INT | Primary key, auto increment |
| first_name | VARCHAR(50) | |
| last_name | VARCHAR(50) | |
| salary | INT | |
| joining_date | DATE | |
| department | VARCHAR(50) | |

**`reward`** – 4 reward records
| Column | Type | Notes |
|--------|------|-------|
| employee_ref_id | INT | Foreign key → employee2(employee_id) |
| date_reward | DATE | |
| amount | INT | |

One employee can receive many rewards (one-to-many).

## 🔍 SQL Concepts Covered
| Topic | Queries | Functions / Keywords |
|-------|---------|----------------------|
| String functions | Q1–Q3 | `LENGTH()`, `REPLACE()`, `CONCAT()` |
| Date functions | Q4, Q24, Q25 | `YEAR()`, `MONTH()`, `DAY()`, `NOW()` |
| Sorting | Q5–Q7 | `ORDER BY` (ASC, DESC, multiple columns) |
| Filtering | Q8–Q10, Q18 | `WHERE`, `IN`, `NOT IN` |
| Pattern matching | Q11–Q15, Q26 | `LIKE` with `%`, `_` and escape character |
| Numeric conditions | Q16–Q17 | `>`, `BETWEEN ... AND` |
| Date filtering | Q20–Q23 | `YEAR()`, `MONTH()`, `<`, `>` on dates |

## 📝 Sample Queries
```sql
-- Employees whose name starts with B
SELECT * FROM employee2 WHERE first_name LIKE 'B%';

-- Salary between 20 lakh and 50 lakh
SELECT * FROM employee2 WHERE salary BETWEEN 2000000 AND 5000000;

-- Employees who joined in 2019
SELECT * FROM employee2 WHERE YEAR(joining_date) = 2019;
```

## 📂 Files
- `employee_reward.sql` – full SQL script (tables, data and all queries)
- `screenshots/` – query outputs (optional)

## ▶️ How to Run
1. Open **MySQL Workbench** and connect to your local MySQL server.
2. Open `employee_reward.sql`.
3. Run the script.

## 👩‍💻 Author
**Shabana Sherin RV** – Data Analytics student
