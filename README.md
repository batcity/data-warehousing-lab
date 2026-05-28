# Data Warehouse Lab

This repository contains hands-on notes and examples for **data warehouse design** and **analytical data modeling** concepts commonly used in OLAP systems.

The goal is to understand how analytical systems are modeled differently from transactional systems (OLTP), and how different warehouse architectures solve scalability, flexibility, and reporting problems.


# Data Modeling Approaches

## 1. Dimensional Modeling

Dimensional modeling is the most common approach used in analytics systems and BI platforms.

It focuses on:
- Fast querying
- Easy reporting
- Business-friendly schemas

### Topics

- [Star Schema](./dimensional-modeling/star-schema/README.md)
- [Snowflake Schema](./dimensional-modeling/snowflake-schema/README.md)
- [Galaxy Schema](./dimensional-modeling/galaxy-schema/README.md)
- [Fact Table Types](./dimensional-modeling/fact-table-types/README.md)
- [Slowly Changing Dimensions (SCD)](./dimensional-modeling/slowly-changing-dimensions/README.md)

### Key Concepts

- Fact tables
- Dimension tables
- Denormalization
- Historical tracking
- Analytical query optimization


## 2. Data Vault Modeling

Data Vault is a modeling methodology designed for:
- Scalability
- Auditability
- Incremental loading
- Enterprise data warehousing

It separates business entities, relationships, and historical changes into:
- Hubs
- Links
- Satellites

### Topics

- [Data Vault Modeling](./data-vault/README.md)

### Planned Topics

- PIT Tables
- Bridge Tables
- Hash Keys
- Raw Vault vs Business Vault

## 3. Inmon Architecture

The Inmon approach, proposed by Bill Inmon, follows a **top-down enterprise data warehouse strategy**.

It focuses on building a centralized, integrated, and normalized Enterprise Data Warehouse (EDW) before creating downstream analytical data marts.

### Key Ideas

- Subject-oriented data organization
- Centralized enterprise warehouse
- Normalized schemas (typically 3NF)
- Data marts built from the EDW
- Strong governance and consistency

### Planned Topics

- Enterprise Data Warehouse (EDW)
- Corporate Information Factory (CIF)
- Normalized warehouse design
- Data marts
- ETL pipelines

## 4. One Big Table (OBT) Modeling

One Big Table (OBT) modeling is a modern analytics approach where data is heavily denormalized into wide tables optimized for fast querying and simplicity.

This approach is commonly used in modern cloud warehouses and analytics stacks.

### Key Ideas

- Wide denormalized tables
- Simpler querying experience
- Reduced joins
- Faster dashboard development
- Trade-offs between storage and performance

### Common Use Cases

- BI dashboards
- Ad-hoc analytics
- ML feature generation
- Startup analytics stacks

### Planned Topics

- Wide table design
- Incremental transformations
- Scan cost trade-offs
- Partitioning strategies
- Query optimization


# Storage & Performance Optimization

These concepts apply across multiple modeling styles.

## Topics

- [Partitioning](./partitioning/README.md)

### Future Topics

- Clustering
- Indexing
- Materialized Views
- Compression
- Columnar Storage


# Sample Data

Datasets and examples used throughout the repository:

- [Sample Data](./sample-data/README.md)

Examples include:
- E-commerce orders
- User activity logs
- Payments
- Inventory events


# Learning Goals

By working through this repository, you should understand:

- How OLAP systems differ from OLTP systems
- How to design dimensional models
- When to use star vs snowflake schemas
- How historical tracking works using SCDs
- Basics of scalable enterprise warehouse modeling


# Recommended Resources

- https://www.exasol.com/hub/data-warehouse/schemas
- [Kimball Dimensional Modeling](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/)
- Designing Data-Intensive Applications
