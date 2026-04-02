# 🐾 Ollie & Hana Puppy Nursery - Database System

### 🎯 Objective
This project involves the design and implementation of a fully normalized, relational database system for **Ollie & Hana Puppy Nursery**, a premium pet care brand. The system was built to manage daily operations—including boarding, grooming, daycare, and training—across multiple branch locations (Jaya One, United Point, and future expansions). 

### 🛠️ Tech Stack & Concepts
* **Database Engine:** Oracle SQL / Oracle APEX
* **Data Modeling:** Entity-Relationship Diagrams (ERD)
* **Architecture:** 3NF (Third Normal Form) Normalization

### 📂 Repository Contents
* **`Ollie&Hanna.sql`**: The complete DDL script defining the 3NF database schema, including all tables, primary keys, foreign keys, and check constraints.
* **`Report.pdf`**: Comprehensive technical documentation detailing the business rules, operational flow, initial unnormalized data models, and the step-by-step normalization process (1NF -> 2NF -> 3NF).

### 🗄️ Database Architecture (3NF)
The database eliminates data redundancy and ensures data integrity by separating entities into distinct, related tables. Key structural features include:
* **Customer & Pet Management:** Customers and their pets are tracked in a one-to-many relationship (`CUSTOMER`, `PET`), capturing essential details like allergies, breed, and health requirements.
* **Branch & Employee Operations:** Tracks staff roles and assigns them to specific geographical branches (`BRANCH`, `EMPLOYEE`).
* **Service Tracking:** Services are categorized with base prices (`SERVICE_TYPE`), handling complex service dependencies and prerequisites (`SERVICE_DEPENDENCY`).
* **Health & Medical Logging:** Dedicated tables for pet health checks and medical logs (`HEALTH_CHECK`, `PET_MEDICAL_LOG`) ensuring the premium safety standards of the nursery are met.
* **Booking & Transactions:** Normalized booking structures (`BOOKING`, `BOOKING_SERVICE_LINE`) and financial ledgers (`TRANSACTION`, `TRANSACTION_SERVICE_LINE`) to process multi-service payments and loyalty point redemption.

### 💡 Key Highlights
* **Robust Constraints:** The SQL schema utilizes strict constraints (e.g., `CHECK (Passed IN (0, 1))` for health checks) to prevent dirty data entry.
* **Scalability:** The architecture was specifically designed to support the brand's long-term goal of opening smaller neighbourhood outlets by strictly separating branch data from core transaction data.
