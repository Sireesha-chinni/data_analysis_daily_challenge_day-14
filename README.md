# SQL Daily Challenge – Day 14: Sales Analysis

A beginner-friendly SQL challenge focused on querying a small `Sales` table. This repo contains the problem statement, the database setup script, and my solutions to all 10 questions.

## Topics Covered

- Creating a database and table (`CREATE DATABASE`, `CREATE TABLE`)
- Inserting data (`INSERT INTO ... VALUES`)
- Selecting all or specific columns (`SELECT`)
- Filtering rows (`WHERE`)
- Sorting results (`ORDER BY` with `ASC` / `DESC`)
- Removing duplicates (`DISTINCT`)

## Repository Structure

```
.
├── Day14_Coding_Challenge.pdf                   # Problem statement
├── day_14_data_analytics_daily_challenge.sql    # Setup script + solutions
└── README.md
```

## Table Schema

**Table:** `Sales`

| Column         | Data Type      | Notes       |
|----------------|----------------|-------------|
| `sale_id`      | INT            | Primary key |
| `customer_name`| VARCHAR(50)    |             |
| `city`         | VARCHAR(50)    |             |
| `product_name` | VARCHAR(50)    |             |
| `category`     | VARCHAR(50)    |             |
| `quantity`     | INT            |             |
| `price`        | DECIMAL(10,2)  |             |
| `sale_date`    | DATE           |             |

## Sample Data

| sale_id | customer_name | city      | product_name | category    | quantity | price | sale_date  |
|---------|---------------|-----------|--------------|-------------|----------|-------|------------|
| 1       | Ravi          | Bangalore | Laptop       | Electronics | 1        | 60000 | 2023-06-01 |
| 2       | Priya         | Chennai   | Mobile       | Electronics | 2        | 20000 | 2023-06-03 |
| 3       | Amit          | Delhi     | Headphones   | Accessories | 3        | 2000  | 2023-06-05 |
| 4       | Neha          | Mumbai    | Chair        | Furniture   | 2        | 5000  | 2023-06-07 |
| 5       | Ravi          | Bangalore | Mobile       | Electronics | 1        | 20000 | 2023-06-10 |
| 6       | Priya         | Chennai   | Laptop       | Electronics | 1        | 60000 | 2023-06-12 |
| 7       | Amit          | Delhi     | Chair        | Furniture   | 4        | 5000  | 2023-06-15 |
| 8       | Neha          | Mumbai    | Headphones   | Accessories | 2        | 2000  | 2023-06-18 |

## Challenge Questions & Solutions

**1. Show all records from the Sales table.**
```sql
SELECT * FROM Sales;
```

**2. Display only customer names and cities.**
```sql
SELECT customer_name, city FROM Sales;
```

**3. Show product name and price.**
```sql
SELECT product_name, price FROM Sales;
```

**4. Show all sales where city is 'Bangalore'.**
```sql
SELECT * FROM Sales
WHERE city = 'Bangalore';
```

**5. Find all products in the 'Electronics' category.**
```sql
SELECT product_name, category FROM Sales
WHERE category = 'Electronics';
```

**6. Show sales where price is greater than 10,000.**
```sql
SELECT * FROM Sales
WHERE price > 10000;
```

**7. Display sales where quantity is more than 2.**
```sql
SELECT * FROM Sales
WHERE quantity > 2;
```

**8. Show all sales sorted by price (low to high).**
```sql
SELECT * FROM Sales
ORDER BY price ASC;
```

**9. Display sales sorted by quantity (high to low).**
```sql
SELECT * FROM Sales
ORDER BY quantity DESC;
```

**10. Show unique cities.**
```sql
SELECT DISTINCT city FROM Sales;
```

## How to Run

1. Install a SQL client and server (this script was written for **MySQL**, e.g. MySQL Workbench).
2. Clone this repository:
   ```bash
   git clone https://github.com/Sireeha-chinni/data_analysis_daily_challenge_day-14.git
   cd data_analysis_daily_challenge_day-14
   ```
3. Open `day_14_data_analytics_daily_challenge.sql` in your SQL client.
4. Run the script from top to bottom. It will create the `DailyChallenge` database, create the `Sales` table, insert the sample data, and run all 10 queries.

Or run it from the command line:
```bash
mysql -u <username> -p < day_14_data_analytics_daily_challenge.sql
```

## Key Takeaways

- `SELECT *` returns every column; naming columns returns only what you need.
- `WHERE` filters rows before they are returned.
- `ORDER BY` sorts ascending by default; add `DESC` for descending.
- `DISTINCT` removes duplicate values from the result.

## Author

**<Ch Sai Sireesha>**
- GitHub: [@Sireesha-chinni](https://github.com/Sireesha-chinni)
- LinkedIn: [Sireesha-Chinni](https://www.linkedin.com/in/sireesha-chinni/)

---

*Part of my Data Analytics Daily Challenge series. Follow along for more!*
