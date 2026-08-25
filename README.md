<div align="center">

# 🗄️ Database Systems Engineering
## & Distributed Backend Development

**25CS1302E · PCC · 4 Credits · Trimester T03**

*Outside-in · Project-driven · Production-minded*

[![Course](https://img.shields.io/badge/Course-25CS1302E-2563eb?style=for-the-badge)](#)
[![PBL](https://img.shields.io/badge/PBL-FULL-7c3aed?style=for-the-badge)](#)
[![CampusConnect](https://img.shields.io/badge/Anchor%20Project-CampusConnect-0f766e?style=for-the-badge)](https://github.com/tejaswin-amara/campus-connect)
[![MySQL](https://img.shields.io/badge/MySQL-8.4%20LTS-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](#)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4.1-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)](#)
[![Java](https://img.shields.io/badge/Java-25-437291?style=for-the-badge&logo=openjdk&logoColor=white)](#)

### Build the data layer. Understand the service. Engineer for scale.

</div>

---

## ✦ About this repository

This repository is the practical workspace for **Database Systems Engineering and Distributed Backend Development (25CS1302E)**.

The course follows an **outside-in learning model**: begin with a working application, then progressively open the layers underneath it—from HTTP and backend services to relational modelling, SQL, transactions, indexing, query execution, and distributed-database fundamentals.

The course anchor is **CampusConnect**, a campus event catalogue and administrative control-plane application. Its current implementation is a **Spring Boot modular monolith backed by MySQL 8.4**, with explicit event, identity, registration-interest, recommendation, and operations boundaries. fileciteturn1file0

> **Core philosophy:** don't just learn how to use a database. Learn how the system behaves, why it behaves that way, and how to engineer it correctly.

---

## 🚀 Anchor Project — CampusConnect

### A Trustworthy Campus Event Catalogue & Management Platform

urlOpen the CampusConnect repositoryhttps://github.com/tejaswin-amara/campus-connect

CampusConnect is the **primary PBL project** used to connect the DBSE&DBD syllabus with a real software system. It gives the course a concrete domain in which database modelling, integrity, SQL, transactions, indexes, backend architecture, security, observability, and scalability can be studied rather than treated as isolated exercises.

The current application provides public event discovery, administrative event management, student-interest tracking, event media persistence, security controls, migrations, health/metrics, Docker support, and CI. fileciteturn1file0

### 🧱 System at a glance

```text
                    ┌───────────────────────┐
                    │  Student / Admin UI   │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌───────────────────────┐
                    │ Spring MVC + Security │
                    │ CSRF · RBAC · Session │
                    └───────────┬───────────┘
                                │
              ┌─────────────────┼──────────────────┐
              ▼                 ▼                  ▼
       ┌────────────┐    ┌─────────────┐    ┌─────────────┐
       │   Events   │    │  Identity   │    │ Registrations│
       │   Service  │    │   Services  │    │ / Interest   │
       └─────┬──────┘    └──────┬──────┘    └──────┬──────┘
             │                  │                  │
             └──────────────────┼──────────────────┘
                                ▼
                    ┌───────────────────────┐
                    │ Spring Data JPA       │
                    │ Hibernate Validation  │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌───────────────────────┐
                    │      MySQL 8.4        │
                    │  Relational Source    │
                    │      of Truth         │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌───────────────────────┐
                    │ Flyway V1 → V3        │
                    │ Schema Evolution      │
                    └───────────────────────┘
```

The current data layer uses MySQL 8.4 as the authoritative transactional store, JPA for the application model, Flyway 12.4.0 for migrations, and `DDL_AUTO=validate` so Hibernate does not silently mutate the production schema. fileciteturn3file0

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
| **Anchor Project** | CampusConnect |
| **Database** | MySQL 8.4 LTS |
| **Backend** | Spring Boot 4.1 · Spring Framework 7 |
| **Runtime** | Java 25 |
| **Persistence** | Spring Data JPA + Hibernate |
| **Migrations** | Flyway 12.4.0 |
| **Build** | Maven 3.9.11 Wrapper |
| **Testing** | JUnit 5 · JaCoCo |
| **Operations** | Docker Compose · Actuator · Micrometer · GitHub Actions |

### 🔗 Official learning material

- 📘 [Self-Learning Material — 25CS1302E](https://y25btech.klef.in/slm/25CS1302E.html)

---

## 🧭 Learning Journey

```text
HTTP / Backend
      │
      ▼
┌─────────────────┐
│ M1 · Service    │  Understand the running system
└────────┬────────┘
         ▼
┌─────────────────┐
│ M2 · Data Model │  ER → relational schema → 3NF/BCNF
└────────┬────────┘
         ▼
┌─────────────────┐
│ M3 · SQL        │  DDL · DML · joins · analytics
└────────┬────────┘
         ▼
┌─────────────────┐
│ M4 · Transactions│ ACID · isolation · concurrency
└────────┬────────┘
         ▼
┌─────────────────┐
│ M5 · Indexing   │  indexes · plans · optimisation
└────────┬────────┘
         ▼
┌─────────────────┐
│ M6 · Distribution│ replication · sharding · CAP
└─────────────────┘
```

---

# 🧩 Module-Wise Syllabus

## M1 · Backend Service as a System

**CO1 · BTL4 — Analyze**

Trace a request through a real application and understand the layers between HTTP and persistence.

- REST resources, verbs, status codes, idempotence and statelessness
- Spring MVC controllers, services and repositories
- Dependency injection at use-site
- JPA/Hibernate as the persistence boundary
- MySQL as the relational source of truth
- End-to-end request tracing
- Modular-monolith boundaries and service responsibilities

**CampusConnect evidence:** event discovery, administration, registration-interest, identity, recommendation and operations boundaries. fileciteturn1file0

---

## M2 · Data Modelling — ER & Normalisation

**CO2 · BTL3 — Apply**

Design a relational model that preserves integrity and avoids unnecessary redundancy.

- Entities, attributes, relationships and cardinality
- Primary, candidate and foreign keys
- Functional dependencies
- 1NF · 2NF · 3NF · BCNF
- Many-to-many relationship resolution
- Surrogate vs natural keys
- Controlled denormalisation

**CampusConnect model:** `USERS` and `EVENTS` are independent entities; `REGISTRATIONS` resolves their many-to-many relationship and stores relationship-specific attributes such as registration date and interest status. fileciteturn3file0

```text
USERS  1 ───────────<  REGISTRATIONS  >─────────── 1  EVENTS
  │                         │                         │
  │ username [UNIQUE]       │ user_id [FK]            │ title
  │ email    [UNIQUE]       │ event_id [FK]           │ date_time
  │ role                    │ status                  │ category
  │                         │ registration_date       │ venue
  └─────────────────────────┴─────────────────────────┘
```

---

## M3 · SQL Fluency

**CO3 · BTL3 — Apply**

Use SQL to define, manipulate, analyse and report on the CampusConnect dataset.

- DDL: `CREATE`, `ALTER`, `DROP`
- DML: `INSERT`, `UPDATE`, `DELETE`
- `SELECT`, filtering and projection
- `INNER`, `LEFT`, `RIGHT`, `FULL` joins
- `GROUP BY`, `HAVING` and aggregates
- Subqueries and CTEs
- Analytical/window functions
- Query cardinality and execution reasoning

### Example CampusConnect query

```sql
SELECT category, COUNT(*) AS event_count
FROM events
WHERE date_time > UTC_TIMESTAMP()
GROUP BY category
ORDER BY event_count DESC;
```

This represents a real catalogue/analytics access pattern documented by the project's data-engineering evidence. fileciteturn3file0

---

## M4 · Transactions & Concurrency

**CO4 · BTL4 — Analyze**

Understand how CampusConnect protects data integrity when multiple requests arrive concurrently.

- ACID properties
- `BEGIN`, `COMMIT`, `ROLLBACK`
- Isolation levels
- Dirty/non-repeatable/phantom reads
- Lost updates and write skew
- Pessimistic locking
- MVCC concepts
- Deadlock awareness
- Short and explicit transaction boundaries
- Idempotent retry design

### 🔐 CampusConnect concurrency case

The current student-interest flow is transactional. The service performs a duplicate check, loads the user, obtains a **pessimistic write lock on the event row**, repeats the duplicate check, and inserts the unique user-event relationship. The database also enforces the uniqueness invariant. fileciteturn3file0

> **Important:** CampusConnect currently records student interest; the configured external registration system remains authoritative for actual seat allocation. `max_capacity` by itself is not a ticketing implementation. fileciteturn3file0

---

## M5 · Indexing & Query Execution

**CO5 · BTL4 — Analyze**

Learn to connect application query patterns to physical database access paths.

CampusConnect's V3 migration adds indexes based on actual catalogue and analytics patterns:

| Index | Why it exists |
|---|---|
| `date_time` | Upcoming/time-based event queries |
| `(category, date_time)` | Category filtering + chronological ordering |
| `(event_id, status)` | Registration analytics by event/status |
| `(user_id, status)` | User/status registration queries |

The project explicitly treats indexes as query-driven engineering decisions rather than speculative additions. fileciteturn3file0

Study alongside:

- B-tree / B+ tree concepts
- Composite indexes
- Covering/index-only access
- `EXPLAIN` and `EXPLAIN ANALYZE`
- Sequential vs index scans
- Join strategies
- Selectivity and statistics
- ORM N+1 query problems
- Measure → diagnose → tune → measure

---

## M6 · Distribution Basics — When One Machine Is Not Enough

**CO6 · BTL3 — Apply**

Use CampusConnect as the baseline for reasoning about future scale rather than falsely claiming distributed infrastructure that is not currently deployed.

- Primary-replica replication
- Synchronous vs asynchronous replication
- Read scaling and replica lag
- Failover
- Horizontal sharding
- Distributed transactions
- Two-phase commit
- CAP theorem
- Polyglot persistence
- Derived vector-search architectures

CampusConnect documents MongoDB, pgvector, Kafka, FastAPI, Node.js and Kubernetes as **bounded evolution paths**, not as current runtime components. fileciteturn1file0

---

# 🏗️ CampusConnect → DBMS Mapping

| DBMS concept | CampusConnect implementation / evidence |
|---|---|
| **Relational modelling** | Users, events and registrations modelled as relational entities |
| **Keys & constraints** | Primary keys, unique usernames/emails, foreign keys, status/capacity checks |
| **Normalisation** | Registration relationship separated from user/event entities |
| **SQL** | Catalogue and registration analytics queries |
| **Transactions** | Transactional student-interest workflow |
| **Concurrency** | Pessimistic event-row locking + unique user-event relationship |
| **Indexing** | Date, category/date, event/status and user/status indexes |
| **Schema evolution** | Flyway V1–V3 migrations |
| **ORM** | Spring Data JPA + Hibernate |
| **Integrity** | Database constraints + application validation |
| **Observability** | Actuator + Micrometer/Prometheus |
| **Deployment** | Dockerfile + Docker Compose |
| **CI** | GitHub Actions |
| **Distributed evolution** | Documented replication, polyglot and extraction paths |

The repository's DBSE&DBD evidence package explicitly maps implementation evidence to CO1–CO6. fileciteturn1file0

---

# 🗓️ 12-Week PBL Build Plan

| Weeks | Module | CampusConnect work |
|---:|---|---|
| **1–2** | M1 | Understand architecture, HTTP flow, Spring layers and persistence boundary |
| **3–4** | M2 | Reverse-engineer ER model, keys, relationships and normalisation |
| **5–6** | M3 | Write DDL/DML, joins, aggregates and analytics queries |
| **7–8** | M4 | Analyse transactions, uniqueness, locking and concurrent interest writes |
| **9–10** | M5 | Study migration indexes and benchmark query access paths |
| **11–12** | M6 | Model replication, sharding, failover and polyglot evolution scenarios |

---

# 🧪 Practical Work

The `Practical/` directory is intended for hands-on DBMS work derived from the course and the anchor project.

Recommended progression:

```text
Practical/
├── 01_ER_Model/
├── 02_Normalisation/
├── 03_SQL/
├── 04_Joins_and_Aggregation/
├── 05_Subqueries_and_CTEs/
├── 06_Transactions/
├── 07_Concurrency/
├── 08_Indexing/
├── 09_Query_Optimisation/
├── 10_Migrations/
├── 11_Distributed_Database_Concepts/
└── 12_CampusConnect_DB_Evidence/
```

Use this area for SQL scripts, schema exercises, query plans, transaction experiments, ER diagrams, screenshots/evidence and project-specific database work.

---

# 🧠 Skills Development

The `Skills/` directory is for focused mastery rather than weekly lab submissions.

```text
Skills/
├── SQL/
├── MySQL/
├── ER-Modelling/
├── Normalisation/
├── Transactions/
├── Concurrency/
├── Indexing/
├── Query-Optimisation/
├── Spring-Data-JPA/
├── Flyway/
└── Distributed-Databases/
```

Each skill should ideally contain:

- 📘 Concept notes
- 💻 Working examples
- 🧪 Exercises
- 🧩 CampusConnect application
- 📈 Performance evidence where applicable
- 📝 Key takeaways

---

# 🎯 Course Outcomes

| CO | Outcome | Level | CampusConnect evidence |
|---|---|---|---|
| **CO1** | Analyze a backend service as a layered system and trace requests end-to-end. | BTL4 | Spring MVC → services → JPA → MySQL |
| **CO2** | Apply ER modelling and normalisation to relational schema design. | BTL3 | Users, events, registrations |
| **CO3** | Apply SQL for definition, manipulation, joins and analytical queries. | BTL3 | Catalogue + registration analytics |
| **CO4** | Analyze transactions, isolation, concurrency anomalies and MVCC. | BTL4 | Transactional interest workflow + pessimistic locking |
| **CO5** | Analyze indexes, query plans and cost-based optimisation. | BTL4 | V3 query indexes + query-pattern analysis |
| **CO6** | Apply replication, sharding and CAP concepts to distributed databases. | BTL3 | Architecture/evolution analysis |

---

# 🛠️ Current Technology Baseline

```text
Frontend / Web
      │
      ▼
Spring MVC + Thymeleaf
      │
      ▼
Spring Security + Application Services
      │
      ▼
Spring Data JPA / Hibernate
      │
      ▼
MySQL 8.4 LTS
      │
      ├── Flyway migrations
      ├── Constraints
      └── Query indexes

Operations
├── Docker / Compose
├── Actuator
├── Micrometer / Prometheus
├── GitHub Actions
└── Automated tests + coverage
```

The current CampusConnect README identifies Java 25, Spring Boot 4.1.0, Spring Framework 7, MySQL 8.4 LTS, Flyway 12.4.0, Maven 3.9.11, JaCoCo, Surefire, Resilience4j, Bucket4j, Actuator and Micrometer as the stable baseline. fileciteturn1file0

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

Make invariants explicit.

Make transactions deliberate.

Measure before optimizing.

Use EXPLAIN, not assumptions.

Treat concurrency as a first-class concern.

Keep the relational database authoritative until
there is a measured reason to introduce another store.

Scale the architecture only when the workload requires it.
```

---

## 🔮 What this course unlocks

```text
                 25CS1302E
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
   🗄️ DB Engineering  ⚙️ Backend  📊 Data Engineering
          │          │          │
          └──────────┼──────────┘
                     ▼
          🏗️ Scalable System Design
                     │
                     ▼
             🤖 Agentic AI Backends
```

The goal is not simply to finish SQL exercises. By the end of the course, you should be able to **design, implement, debug, measure and defend a production-style data-backed backend system**—using CampusConnect as the concrete engineering case study.

---

<div align="center">

### Built for learning. Structured for engineering. Ready for scale.

**25CS1302E · Database Systems Engineering & Distributed Backend Development**

urlCampusConnect Anchor Projecthttps://github.com/tejaswin-amara/campus-connect

</div>
