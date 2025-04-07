# SQL Server Data Warehouse: ERP + CRM Integration (Medallion Architecture)

A robust SQL Server-based data warehouse built for batch ETL processing of enterprise data from ERP and CRM systems. This project follows a modern Medallion Architecture (Bronze → Silver → Gold) and applies data quality checks, enforce business rules, and dimensional modeling to prepare data for advanced analytics and reporting.

1. Created stored procedures and views to automate ETL batch processing of data from two sources — ERP and CRM — into the SQL Server data warehouse.
2. Authored SQL scripts to implement data quality checks and business rules, ensuring data consistency and integration across Silver and Gold layers.
3. Documented data architecture, lineage, and catalog to maintain a reliable central source of truth for downstream data consumers.
4. Applied business logic and data integration techniques to model data using STAR schema, resulting in structured and analytics-ready datasets.
5. Performed analytical tasks such as performance analysis, cumulative metrics, rankings, and customer segmentation to support advanced reporting needs.
6. Developed detailed reports to uncover insights about customer behavior and product performance, supporting stakeholders in strategic and operational decision-making.

---

##  Tools Used

- SQL Server Express, SQL Server Management Studio (SSMS), SQL, Github, Notion, Draw.io 

---
## This Project Involves:

### 1. Data Architecture
Designing a layered data warehouse using Medallion Architecture with Bronze, Silver, and Gold layers to organize raw, cleaned, and business-modeled data respectively.

![DataArchitecture](https://github.com/LikhithaGuggilla/SQL-Data-Warehouse-Project/blob/main/docs/data_architecture.png)

### 2. ETL Pipelines
Automating the extraction, transformation, and loading of data from ERP and CRM systems using stored procedures and SQL scripts.

![DataLineage](https://github.com/LikhithaGuggilla/SQL-Data-Warehouse-Project/blob/main/docs/data_flow.png)

### 3. Data Modeling
Creating dimension and fact tables based on identified relationships across source systems. The Gold layer is modeled using STAR schema to support analytical queries.

![DataModeling](https://github.com/LikhithaGuggilla/SQL-Data-Warehouse-Project/blob/main/docs/data_model.png)

### 4. Analytics & Reporting
Building SQL-based reports to help analyze customer behavior, product performance, and sales trends, enabling stakeholders to make informed, data-driven decisions.

Review the [Data Catalog](https://github.com/LikhithaGuggilla/SQL-Data-Warehouse-Project/blob/main/docs/data_catalog.md)

--
## Repository Structure

```
SQL-Data-Warehouse-Project/
│
├── datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── docs/                               # Project documentation and architecture details
│   ├── etl.drawio                      # Draw.io file shows all different techniquies and methods of ETL
│   ├── data_architecture.drawio        # Draw.io file shows the project's architecture
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   ├── data_flow.drawio                # Draw.io file for the data flow diagram
│   ├── data_models.drawio              # Draw.io file for data models (star schema)
│   ├── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── scripts/                            # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   ├── gold/                           # Scripts for creating analytical models
│
├── tests/                              # Test scripts and quality files
│
├── README.md                           # Project overview 
├── LICENSE                             # License information for the repository

```

## Setup & Run

1. Clone repo.
2. Open SSMS.
3. Execute `ini_database.sql`in the `scripts` folder
4. Execute ddl scripts in `bronze`, `silver`, `gold` folders in the specified order:
 - `ddl_bronze.sql`
- `ddl_silver.sql`
-`ddl_gold.sql` 
4. Run stored procedures in order:
   - `procedure_load_bronze.sql`
   - `procedure_load_silver.sql`
5. Run data quality check scripts in `tests`folder:
- `quality_checks_silver.sql`
- `quality_checks_gold.sql`

