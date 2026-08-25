<div align="center">

# 🗄️ Database Systems Engineering
## & Distributed Backend Development

**25CS1302E · PCC · 4 Credits · Trimester T03**

*Outside-in · Project-driven · Production-minded*

[![Course](https://img.shields.io/badge/Course-25CS1302E-2563eb?style=for-the-badge)](#)
[![PBL](https://img.shields.io/badge/PBL-FULL-7c3aed?style=for-the-badge)](#)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-336791?style=for-the-badge&logo=postgresql&logoColor=white)](#)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3-6db33f?style=for-the-badge&logo=springboot&logoColor=white)](#)
[![Java](https://img.shields.io/badge/JDK-21-007396?style=for-the-badge&logo=openjdk&logoColor=white)](#)

### Build the data layer. Understand the service. Engineer for scale.

</div>

---

## ✦ What is this repository?

This repository is the practical workspace for **Database Systems Engineering and Distributed Backend Development (25CS1302E)**.

The course follows an **outside-in learning model**: start with a working backend service, then progressively open the layers underneath it—from HTTP and REST to relational modelling, SQL, transactions, indexes, query execution, replication, sharding, and CAP.

> **Core philosophy:** don't just learn how to use a database. Learn how the system behaves, why it behaves that way, and how to engineer it correctly.

---

## 📚 Course at a Glance

| | Details |
|---|---|
| **Course** | Database Systems Engineering and Distributed Backend Development |
| **Code** | `25CS1302E` |
| **Type** | PCC · Project-Based Learning |
| **Credits** | 4 |
| **Contact** | 8 hours/week |
| **Trimester** | T03 |
| **Prerequisites** | DSA-1 · PSPJ |
| **Primary Database** | PostgreSQL 16 |
| **Backend** | Spring Boot 3 |
| **Runtime** | JDK 21 LTS |
| **Build** | Maven |
| **Testing** | JUnit 5 · Testcontainers |
| **API Testing** | Postman / Bruno |

### 🔗 Official learning material

- 📘 [Self-Learning Material — 25CS1302E](https://y25btech.klef.in/slm/25CS1302E.html)

---

## 🧭 Learning Journey

```text
HTTP Request
     │
     ▼
┌───────────────┐
│ REST / Spring │  M1 · Backend as a System
└───────┬───────┘
        ▼
┌───────────────┐
│ ER + Schema   │  M2 · Data Modelling
└───────┬───────┘
        ▼
┌───────────────┐
│ SQL           │  M3 · Query Fluency
└───────┬───────┘
        ▼
┌───────────────┐
│ Transactions  │  M4 · ACID + Concurrency
└───────┬───────┘
        ▼
┌───────────────┐
│ Index + Plans  │  M5 · Query Execution
└───────┬───────┘
        ▼
┌───────────────┐
│ Distribution  │  M6 · Replication + Sharding
└───────────────┘
```

---

# 🧩 Modules

## M1 · Backend Service as a System

**CO1 · BTL4 — Analyze**

Understand a backend as a layered system and trace a request from HTTP arrival to JSON response.

- REST resources, verbs, status codes, idempotence and statelessness
- Spring Boot `@RestController`, `@Service`, `@Repository`
- Dependency injection at use-site
- PostgreSQL and `psql`
- HTTP → routing → service → data access → ORM/JDBC → SQL → storage
- End-to-end request tracing with `GET /books/{id}`

---

## M2 · Data Modelling — ER & Normalisation

**CO2 · BTL3 — Apply**

Design relational schemas that avoid unnecessary redundancy and update anomalies.

- ER diagrams and relationship cardinality
- One-to-one, one-to-many and many-to-many mappings
- Primary, candidate and foreign keys
- Surrogate vs natural keys
- Functional dependencies
- 1NF · 2NF · 3NF · BCNF
- Controlled denormalisation and trade-offs

---

## M3 · SQL Fluency

**CO3 · BTL3 — Apply**

Use SQL confidently for schema definition, manipulation, analytical queries and reporting.

- DDL: `CREATE`, `ALTER`, `DROP`
- DML: `INSERT`, `UPDATE`, `DELETE`
- `SELECT`, projection, selection and joins
- `INNER`, `LEFT`, `RIGHT`, `FULL` joins
- `GROUP BY`, `HAVING` and aggregates
- Scalar, `IN`, `EXISTS` and correlated subqueries
- CTEs and recursive CTEs
- `ROW_NUMBER`, `RANK`, `LAG`, `LEAD`

> **SQL discipline:** always understand the rows being selected, the joins being performed, and the cardinality produced.

---

## M4 · Transactions & Concurrency

**CO4 · BTL4 — Analyze**

Understand how databases preserve correctness when multiple operations execute concurrently.

- ACID properties
- `BEGIN`, `COMMIT`, `ROLLBACK`
- Read Uncommitted · Read Committed · Repeatable Read · Serializable
- Dirty reads, non-repeatable reads and phantom reads
- Lost updates and write skew
- Shared/exclusive locks and two-phase locking
- Deadlocks and detection
- MVCC and PostgreSQL snapshots
- Short, well-defined transaction boundaries

---

## M5 · Indexing & Query Execution

**CO5 · BTL4 — Analyze**

Learn to make queries fast by understanding how PostgreSQL actually executes them.

- B-tree / B+ tree concepts
- Hash indexes
- Multi-column indexes
- Covering indexes and index-only scans
- `EXPLAIN` and `EXPLAIN ANALYZE`
- Sequential, index and index-only scans
- Nested-loop, hash and merge joins
- Cost-based optimisation and statistics
- N+1 queries and ORM performance pitfalls
- Measure → diagnose → tune → measure

---

## M6 · Distribution Basics

**CO6 · BTL3 — Apply**

Reason about databases when storage, throughput or availability requirements exceed a single machine.

- Primary-replica replication
- Synchronous vs asynchronous replication
- Replica lag
- Read scaling
- Failover concepts
- Horizontal sharding by range, hash and lookup table
- Rebalancing challenges
- Distributed transactions and two-phase commit
- CAP theorem
- Introductory NoSQL design choices

---

# 🚀 Anchor Project — BookStash

### A Personal Library Backend Service

> **A REST backend with PostgreSQL — properly modelled, properly indexed, properly transactional.**

**BookStash** is the course's 12-week project. It evolves alongside the modules so that every major concept becomes an engineering decision in a real backend.

### 🏗️ Build progression

| Week | Focus | Project milestone |
|---:|---|---|
| 1–2 | M1 | Working REST service + request tracing |
| 3–4 | M2 | ER model + normalised relational schema |
| 5–6 | M3 | SQL schema + data + reporting queries |
| 7–8 | M4 | ACID borrow/return workflow + concurrency safety |
| 9–10 | M5 | Indexes + EXPLAIN ANALYZE before/after |
| 11–12 | M6 | Replication/read scaling concept or implementation |

### ✨ Functional scope

- 📚 Book CRUD
- 👤 User CRUD
- 🔄 Borrow and return workflows
- 🔎 Search by title, author and ISBN
- 📊 Top-borrowed and overdue reports
- 🔐 Transactionally safe borrow/return logic
- ⚡ Hand-designed indexes for common queries
- 🔁 Idempotent borrow/return retries
- 🧪 Testcontainers integration tests
- 📮 Complete Postman / Bruno collection
- 📈 SQL performance log with `EXPLAIN ANALYZE`
- 📝 Defendable architecture and database design report

### 🛠️ Minimal toolchain

```text
Java 21 LTS
   │
Spring Boot 3 + Spring Data JPA
   │
Maven ─────────────── JUnit 5
   │                       │
PostgreSQL 16 ◄──── Testcontainers
   │
Docker
   │
Git + GitHub
   │
Postman / Bruno
```

### 🎯 Final deliverable

A GitHub repository containing:

- Spring Boot backend
- Flyway or Liquibase migrations
- PostgreSQL schema and seed data
- API collection
- Testcontainers integration tests
- SQL query log
- `EXPLAIN ANALYZE` performance captures
- Database and transaction design report
- Live demonstration of borrow/return flows
- Concurrent-borrow stress demonstration

---

# 🗂️ Repository Structure

```text
DBMS/
│
├── 📁 Practical/
│   ├── Week-01/
│   ├── Week-02/
│   ├── Week-03/
│   └── ...
│
├── 📁 Skills/
│   ├── SQL/
│   ├── PostgreSQL/
│   ├── Spring-Boot/
│   ├── Transactions/
│   ├── Indexing/
│   └── Distributed-DB/
│
└── 📄 README.md
```

### `Practical/`
Hands-on laboratory work, SQL programs, schema exercises, query experiments and project implementation work.

### `Skills/`
Focused skill-building material: SQL fluency, PostgreSQL internals, transaction reasoning, indexing, query optimisation and distributed database concepts.

---

# 🎯 Course Outcomes

| CO | Outcome | Level |
|---|---|---|
| **CO1** | Analyze a backend service as a layered system and trace requests end-to-end. | BTL4 |
| **CO2** | Apply ER modelling and normalisation to relational schema design. | BTL3 |
| **CO3** | Apply SQL for data definition, manipulation, joins and analytical queries. | BTL3 |
| **CO4** | Analyze transactions, isolation, concurrency anomalies and MVCC. | BTL4 |
| **CO5** | Analyze indexes, query plans and cost-based query optimisation. | BTL4 |
| **CO6** | Apply replication, sharding and CAP concepts to distributed databases. | BTL3 |

---

# 📖 Recommended References

1. **Database System Concepts** — Abraham Silberschatz, Henry F. Korth & S. Sudarshan
2. **Designing Data-Intensive Applications** — Martin Kleppmann
3. **Database Internals** — Alex Petrov
4. **PostgreSQL: Up and Running** — Regina O. Obe & Leo S. Hsu
5. **SQL Cookbook** — Anthony Molinaro & Robert de Graaf
6. **Spring in Action** — Craig Walls
7. **Fundamentals of Database Systems** — Ramez Elmasri & Shamkant B. Navathe

---

# 🌐 Learning Resources

| Resource | Focus |
|---|---|
| [IBM Data Engineering · Coursera](https://www.coursera.org/professional-certificates/ibm-data-engineer) | Data engineering foundations |
| [Meta Database Engineer · Coursera](https://www.coursera.org/professional-certificates/meta-database-engineer) | SQL + database engineering |
| [NPTEL — Fundamentals of Database Systems](https://nptel.ac.in/courses/106104135) | Database fundamentals |
| [NPTEL — Distributed Systems](https://nptel.ac.in/courses/106106168) | Distributed backend concepts |
| [System Design Primer](https://github.com/donnemartin/system-design-primer) | Scalable systems and architecture |

---

# 🧠 Engineering Principles

```text
Model before coding.

Normalize by default.

Make transactions explicit.

Measure before optimizing.

Use EXPLAIN, not assumptions.

Design for correctness before scale.

Treat concurrency as a first-class concern.

Know when a single database is enough.
```

---

## 🔮 What this course unlocks

```text
25CS1302E
   │
   ├── 🗄️ Database Engineering
   ├── ⚙️ Backend Engineering
   ├── 📊 Big Data Engineering
   ├── 🏗️ System Design for Scalability
   └── 🤖 Agentic AI Backends
```

The goal is not simply to finish SQL exercises. By the end of the course, you should be able to **design, implement, debug, measure and defend a production-style data-backed backend system.**

---

<div align="center">

### Built for learning. Structured for engineering. Ready for scale.

**25CS1302E · Database Systems Engineering & Distributed Backend Development**

</div>
