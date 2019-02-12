# AWS Databases

## Relational
Relational databases store data with pre-defined schema and relationships between them, designed for supporting ACID transactions, maintaining referential integrity, and data consistency.

Used for: Traditional applications, ERP, CRM, and e-commerce.

- Amazon Aurora: MySQL, PostgreSQL
- Amazon RDS: SQL, PostgreSQL, MariaDB, Oracle, SQL Server
- Amazon Redshift

## Key-value

Key-value databases are optimized to store and retrieve key-value pairs in large volumes and in milliseconds, without the performance overhead and scale limitations of relational databases.

Used for: Internet-scale applications, real-time bidding, shopping carts, and customer preferences.

- Amazon DynamoDB

## Document

Document databases are designed to store semi-structured data as documents and are intuitive for developers to use because the data is typically represented as a readable document.

Used for: Content management, personalization, and mobile applications.

- Amazon DocumentDB (with MongoDB compatibility)

## In-memory

In-memory databases are used for applications that require real time access to data. By storing data directly in memory, these databases provide microsecond latency where millisecond latency is not enough. 

Used for: Caching, gaming leaderboards, and real-time analytics.

- Amazon ElastiCache for Redis
- Amazon ElastiCache for Memcached

## Graph

Graph databases are used for applications that need to enable millions of users to query and navigate relationships between highly connected, graph datasets with millisecond latency.

Used for: Fraud detection, social networking, and recommendation engines

- Amazon Neptune

## Time Series

Time series databases are used to efficiently collect, synthesize, and derive insights from enormous amounts of data that changes over time (known as time-series data).

Used for: IoT applications, DevOps, and industrial telemetry.

- Amazon Timestream

## Ledger

Ledger databases are used when you need a centralized, trusted authority to maintain a scalable, complete and cryptographically verifiable record of transactions.
Used for: Systems of record, supply chain, registrations, and banking transactions.

- Amazon Quantum Ledger Database (QLDB)

---

## _Exam Tips_

