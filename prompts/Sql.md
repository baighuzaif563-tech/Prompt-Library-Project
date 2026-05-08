# 🗄️ SQL Prompt Library — Developer Edition

> A structured collection of **high-quality AI prompts** for SQL & Database concepts  
> Built for **interviews, backend development, and data mastery** 🚀

<br>

## 📋 Table of Contents

- [How to Use](#-how-to-use)
- [Prompt Quality Guide](#-prompt-quality-guide)
- [1. SQL Basics](#-1-sql-basics)
- [2. Filtering & Sorting](#-2-filtering--sorting)
- [3. Joins](#-3-joins)
- [4. Aggregations & Group By](#-4-aggregations--group-by)
- [5. Subqueries & CTEs](#-5-subqueries--ctes)
- [6. Window Functions](#-6-window-functions)
- [7. Indexes & Performance](#-7-indexes--performance)
- [8. Database Design & Normalization](#-8-database-design--normalization)
- [9. Transactions & ACID](#-9-transactions--acid)
- [10. SQL Interview Practice](#-10-sql-interview-practice)
- [11. Master SQL Prompt](#-11-master-sql-prompt)
- [Final Goal](#-final-goal)

---

## 🎯 How to Use

```
1. Pick a topic from the list
2. Copy the ✅ Good Prompt
3. Paste into your AI tool (Claude, ChatGPT, etc.)
4. Get structured explanation + SQL queries
5. Practice on real databases (use SQLiteOnline or DB Fiddle)
```

---

## ⚡ Prompt Quality Guide

| Badge | Meaning |
|-------|---------|
| ✅ **Good Prompt** | Structured, deep explanation, interview-ready output |
| ❌ **Bad Prompt** | Vague, short, produces low-quality response |

> **Rule of Thumb:** Always mention the database (MySQL/PostgreSQL) and ask for sample data.

---

## 📋 1. SQL Basics

### DDL & DML Commands

| | Prompt |
|--|--------|
| ✅ | `Explain SQL DDL and DML commands — CREATE, ALTER, DROP, INSERT, UPDATE, DELETE — with syntax, real examples using a sample 'employees' table, and common mistakes to avoid.` |
| ❌ | `Explain SQL commands.` |

<details>
<summary>📌 Expected Output</summary>

- DDL vs DML vs DCL distinction
- CREATE TABLE with constraints
- INSERT, UPDATE, DELETE with WHERE
- ALTER TABLE for schema changes
- Common pitfalls (DELETE without WHERE, etc.)

</details>

---

### Data Types

| | Prompt |
|--|--------|
| ✅ | `Explain SQL data types in MySQL and PostgreSQL — INT, VARCHAR, TEXT, DATE, TIMESTAMP, BOOLEAN, JSON — with when to use each, storage size, and real examples.` |
| ❌ | `Explain SQL data types.` |

<details>
<summary>📌 Expected Output</summary>

- Numeric types (INT, BIGINT, DECIMAL, FLOAT)
- String types (CHAR vs VARCHAR vs TEXT)
- Date and time types
- JSON and ARRAY (PostgreSQL)
- Choosing the right type for performance

</details>

---

### Constraints

| | Prompt |
|--|--------|
| ✅ | `Explain SQL constraints — PRIMARY KEY, FOREIGN KEY, UNIQUE, NOT NULL, CHECK, DEFAULT — with syntax, real-world use cases, and how they enforce data integrity.` |
| ❌ | `What are SQL constraints?` |

<details>
<summary>📌 Expected Output</summary>

- Each constraint with CREATE TABLE syntax
- Foreign key with ON DELETE CASCADE
- Composite primary keys
- CHECK constraint examples
- How constraints affect performance

</details>

---

## 🔍 2. Filtering & Sorting

### WHERE Clause

| | Prompt |
|--|--------|
| ✅ | `Explain the SQL WHERE clause with all operators — =, !=, >, <, BETWEEN, IN, NOT IN, LIKE, IS NULL, IS NOT NULL — with a sample table, query examples, and performance tips.` |
| ❌ | `Explain WHERE clause.` |

<details>
<summary>📌 Expected Output</summary>

- All comparison operators
- LIKE with wildcard patterns (%, _)
- IN vs multiple OR conditions
- NULL handling (IS NULL vs = NULL)
- Operator precedence with AND/OR

</details>

---

### ORDER BY & LIMIT

| | Prompt |
|--|--------|
| ✅ | `Explain ORDER BY and LIMIT/OFFSET in SQL with examples for pagination, multi-column sorting, NULL ordering behavior, and performance impact on large tables.` |
| ❌ | `Explain ORDER BY.` |

<details>
<summary>📌 Expected Output</summary>

- Single and multi-column ORDER BY
- ASC vs DESC
- LIMIT + OFFSET for pagination
- NULLS FIRST / NULLS LAST
- Why ORDER BY without index is slow

</details>

---

## 🔗 3. Joins

### All Join Types

| | Prompt |
|--|--------|
| ✅ | `Explain all SQL JOIN types — INNER, LEFT, RIGHT, FULL OUTER, CROSS, SELF — with Venn diagram descriptions, sample data, query examples, and when to use each type in real-world scenarios.` |
| ❌ | `Explain SQL joins.` |

<details>
<summary>📌 Expected Output</summary>

- INNER JOIN (matching rows only)
- LEFT JOIN (all left + matching right)
- RIGHT JOIN (all right + matching left)
- FULL OUTER JOIN
- CROSS JOIN (cartesian product)
- SELF JOIN with employee-manager example

</details>

---

### Join Performance

| | Prompt |
|--|--------|
| ✅ | `Explain how SQL joins work internally — hash join, nested loop join, merge join — and how to optimize join queries with proper indexing, join order, and query plan analysis using EXPLAIN.` |
| ❌ | `How to optimize joins?` |

<details>
<summary>📌 Expected Output</summary>

- Hash join vs nested loop vs merge join
- When the query optimizer picks each
- Index on join columns
- EXPLAIN / EXPLAIN ANALYZE output
- Avoiding cartesian joins accidentally

</details>

---

## 📊 4. Aggregations & Group By

### Aggregate Functions

| | Prompt |
|--|--------|
| ✅ | `Explain SQL aggregate functions — COUNT, SUM, AVG, MIN, MAX — with GROUP BY, HAVING, filtering nulls, and real business query examples like total sales per region.` |
| ❌ | `Explain GROUP BY.` |

<details>
<summary>📌 Expected Output</summary>

- COUNT(*) vs COUNT(column)
- SUM and AVG with NULL handling
- GROUP BY with multiple columns
- HAVING vs WHERE (key difference)
- Nested aggregation examples

</details>

---

### ROLLUP & CUBE

| | Prompt |
|--|--------|
| ✅ | `Explain SQL GROUP BY ROLLUP and CUBE — how they generate subtotals and grand totals, the difference between them, and practical examples for sales reporting.` |
| ❌ | `What is ROLLUP in SQL?` |

<details>
<summary>📌 Expected Output</summary>

- ROLLUP hierarchy explained
- CUBE all-combinations explained
- GROUPING() function to detect subtotal rows
- Use in reporting dashboards
- MySQL vs PostgreSQL syntax differences

</details>

---

## 🧩 5. Subqueries & CTEs

### Subqueries

| | Prompt |
|--|--------|
| ✅ | `Explain SQL subqueries — scalar, row, table, correlated — with examples for each type, when to use subqueries vs joins, and performance considerations.` |
| ❌ | `What is a subquery?` |

<details>
<summary>📌 Expected Output</summary>

- Scalar subquery (returns one value)
- Correlated vs non-correlated
- Subquery in SELECT, WHERE, FROM
- EXISTS vs IN performance
- When joins outperform subqueries

</details>

---

### CTEs (Common Table Expressions)

| | Prompt |
|--|--------|
| ✅ | `Explain SQL CTEs (WITH clause) — regular CTEs, multiple CTEs, recursive CTEs — with syntax, use cases like hierarchical data (org charts), and comparison to subqueries and temp tables.` |
| ❌ | `What is a CTE?` |

<details>
<summary>📌 Expected Output</summary>

- CTE syntax and readability benefits
- Multiple CTEs chained together
- Recursive CTE for tree structures
- CTE vs subquery vs temp table
- Employee hierarchy example

</details>

---

## 🪟 6. Window Functions

### Window Function Basics

| | Prompt |
|--|--------|
| ✅ | `Explain SQL window functions — ROW_NUMBER, RANK, DENSE_RANK, NTILE, LAG, LEAD, SUM OVER, AVG OVER — with PARTITION BY and ORDER BY, real examples, and how they differ from GROUP BY.` |
| ❌ | `What are window functions?` |

<details>
<summary>📌 Expected Output</summary>

- OVER clause anatomy
- PARTITION BY vs GROUP BY
- ROW_NUMBER vs RANK vs DENSE_RANK
- LAG and LEAD for row comparison
- Running totals with SUM OVER

</details>

---

### Advanced Window Functions

| | Prompt |
|--|--------|
| ✅ | `Explain advanced SQL window function use cases — top N per group, running totals, moving averages, gap and island problems — with complete query solutions and explanations.` |
| ❌ | `Advanced window functions examples.` |

<details>
<summary>📌 Expected Output</summary>

- Top 3 salaries per department
- 7-day rolling average
- Cumulative percentage
- Gap and island detection
- First/last value per group

</details>

---

## ⚡ 7. Indexes & Performance

### Index Types

| | Prompt |
|--|--------|
| ✅ | `Explain SQL indexes — B-Tree, Hash, Composite, Covering, Partial indexes — how they work internally, when to create them, when they hurt performance, and how to read EXPLAIN output.` |
| ❌ | `Explain SQL indexes.` |

<details>
<summary>📌 Expected Output</summary>

- B-Tree structure explained simply
- When index is used vs skipped
- Composite index column order matters
- Covering index for index-only scans
- Index on high cardinality columns

</details>

---

### Query Optimization

| | Prompt |
|--|--------|
| ✅ | `Explain SQL query optimization techniques — avoiding SELECT *, using indexes, avoiding functions in WHERE, query plan analysis with EXPLAIN, partitioning, and connection pooling with examples.` |
| ❌ | `How to optimize SQL queries?` |

<details>
<summary>📌 Expected Output</summary>

- SELECT * vs explicit columns
- SARGable vs non-SARGable predicates
- Index on WHERE and JOIN columns
- EXPLAIN ANALYZE output reading
- Partitioning for large tables

</details>

---

## 🏗️ 8. Database Design & Normalization

### Normalization

| | Prompt |
|--|--------|
| ✅ | `Explain database normalization — 1NF, 2NF, 3NF, BCNF — with a step-by-step example of taking an unnormalized table all the way to 3NF, and when denormalization is intentional.` |
| ❌ | `Explain normalization.` |

<details>
<summary>📌 Expected Output</summary>

- Unnormalized table example
- 1NF: atomic values, no repeating groups
- 2NF: remove partial dependencies
- 3NF: remove transitive dependencies
- When to intentionally denormalize

</details>

---

### ER Diagrams & Schema Design

| | Prompt |
|--|--------|
| ✅ | `Design a relational database schema for an e-commerce application — include tables for users, products, orders, order_items, payments, and reviews — explain relationships, foreign keys, and indexing strategy.` |
| ❌ | `Design an e-commerce database.` |

<details>
<summary>📌 Expected Output</summary>

- Full CREATE TABLE statements
- Foreign key relationships
- One-to-many and many-to-many design
- Junction/bridge table pattern
- Index recommendations

</details>

---

## 🔒 9. Transactions & ACID

### ACID Properties

| | Prompt |
|--|--------|
| ✅ | `Explain ACID properties in databases — Atomicity, Consistency, Isolation, Durability — with real-world examples (bank transfer), how each property is enforced, and what happens when they're violated.` |
| ❌ | `What is ACID?` |

<details>
<summary>📌 Expected Output</summary>

- Bank transfer atomicity example
- Consistency constraints
- Isolation levels (Read Uncommitted → Serializable)
- Durability via WAL / redo logs
- Dirty read, phantom read, non-repeatable read

</details>

---

### Transactions & Locks

| | Prompt |
|--|--------|
| ✅ | `Explain SQL transactions and locking — BEGIN, COMMIT, ROLLBACK, SAVEPOINT, row-level vs table-level locks, deadlocks, and isolation levels with practical examples in PostgreSQL.` |
| ❌ | `Explain transactions.` |

<details>
<summary>📌 Expected Output</summary>

- BEGIN / COMMIT / ROLLBACK syntax
- Savepoints for partial rollback
- Optimistic vs pessimistic locking
- How deadlocks happen and prevention
- Isolation level tradeoffs

</details>

---

## 🧪 10. SQL Interview Practice

### SQL Mock Interview

| | Prompt |
|--|--------|
| ✅ | `Act as a SQL interviewer at a tech company. Give me progressively harder SQL problems — starting from basic SELECT queries, through joins and aggregations, up to window functions and optimization — with a sample schema. Evaluate my queries and suggest improvements.` |
| ❌ | `Give me SQL interview questions.` |

<details>
<summary>📌 Expected Output</summary>

- Sample tables with data
- Easy → medium → hard progression
- Real interview-style problems
- Query evaluation + feedback
- Common follow-up questions

</details>

---

### Top SQL Interview Questions

| | Prompt |
|--|--------|
| ✅ | `List the top 20 SQL interview questions asked at FAANG companies with complete solutions, edge cases, and explanation of why each question is asked — include window functions, CTEs, and optimization questions.` |
| ❌ | `SQL interview questions.` |

<details>
<summary>📌 Expected Output</summary>

- Nth highest salary problem
- Duplicate detection
- Running totals and moving averages
- Self join problems
- Consecutive dates and gaps

</details>

---

## 🚀 11. Master SQL Prompt

### The Ultimate All-in-One Prompt

```
Teach me SQL from beginner to advanced — cover:
DDL/DML commands, data types, constraints, filtering, joins (all types),
aggregations, GROUP BY, subqueries, CTEs, window functions, indexes,
query optimization, database design, normalization, transactions, and ACID.
Use PostgreSQL syntax, include sample tables with data, real-world examples,
dry runs, and interview-level practice problems.
```

> ❌ **Bad version:** `Teach me SQL.`

<details>
<summary>📌 Expected Output</summary>

- Full structured roadmap
- Concept + query for every topic
- Sample database to practice on
- Performance tuning guidance
- Interview question bank

</details>

---

## 🏁 Final Goal

This prompt library helps you:

| Goal | What it does |
|------|-------------|
| 💼 Interview Ready | Crack data analyst & backend engineer SQL rounds |
| 🧠 Query Writing | Write efficient, clean SQL confidently |
| 🏗️ Schema Design | Design normalized, scalable databases |
| ⚡ Performance | Optimize slow queries and understand indexes |
| 📊 Data Analysis | Answer complex business questions with SQL |

---

## 🔥 Pro Tips

> **Daily Practice Formula:**
> ```
> 1 topic/day + 2 practice queries = SQL-proficient in weeks
> ```

- Practice on real tools: **DB Fiddle**, **SQLiteOnline**, **LeetCode SQL**, **StrataScratch**
- Always look at the **EXPLAIN plan** for your queries
- Learn **window functions** — they appear in almost every advanced interview
- Master the **employee salary** and **ranking** query patterns
- Understand **NULL behavior** — it trips up even experienced developers

---

## 🤝 Contributing

Have a better prompt? Found a pattern that works well?

1. Fork this repo
2. Add your prompt in the relevant section
3. Follow the `✅ Good Prompt / ❌ Bad Prompt / 📌 Expected Output` format
4. Open a Pull Request

---

## ⭐ Star This Repo

If this helped you, please give it a ⭐ — it helps others find it too!

---

<p align="center">Made with ❤️ for every developer on their SQL journey</p>
