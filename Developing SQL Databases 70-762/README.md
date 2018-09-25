https://www.microsoft.com/en-us/learning/exam-70-762.aspx
Nearly everything copied directly from microsoft docs where possible, links provided where I saw fit.


# Design and implement database objects (25–30%)

## Design and implement a relational database schema

### Design Tables And Schemas Based On Business Requirements
### [Improve The Design Of Tables By Using Normalization](https://support.microsoft.com/en-us/help/283878/description-of-the-database-normalization-basics)
### [Write Table Create Statements](https://docs.microsoft.com/en-us/sql/t-sql/statements/create-table-transact-sql?view=sql-server-2017)

Syntax
```sql
--Simple CREATE TABLE Syntax (common if not using options)  
CREATE TABLE   
    [ database_name . [ schema_name ] . | schema_name . ] table_name   
    ( { <column_definition> } [ ,...n ] )   
[ ; ]
```

Example:

```sql
CREATE TABLE Persons (
    PersonID int,
    LastName varchar(255),
    FirstName varchar(255),
    Address varchar(255),
    City varchar(255) 
);
```
[Source](https://www.w3schools.com/sql/sql_create_table.asp)

### [Determine The Most Efficient Data Types To Use](https://docs.microsoft.com/en-us/sql/t-sql/data-types/data-types-transact-sql?view=sql-server-2017)

**Exact Numerics**: bigint, numeric, bit, smallint, decimal, smallmoney, int, tinyint, money

**Approximate numerics**: float, real

**Date and time**: date, datetimeoffset, datetime2, smalldatetime, datetime, time

**Character strings**: char, varchar, text

**Unicode character strings**: nchar, nvarchar, ntext

**Binary strings**: binary, varbinary, image


## Design and implement indexes

### Design New Indexes Based On Provided Tables; Queries; Or Plans
[Columnstore indexes: Overview](https://docs.microsoft.com/en-us/sql/relational-databases/indexes/columnstore-indexes-overview?view=sql-server-2017)

### Distinguish Between Indexed Columns And Included Columns
### Implement Clustered Index Columns By Using Best Practices
### Recommend New Indexes Based On Query Plans

## Design and implement views

### Design A View Structure To Select Data Based On User Or Business Requirements
### Identify The Steps Necessary To Design An Updateable View
### Implement Partitioned Views
### Implement Indexed Views

## Implement columnstore indexes

### Determine Use Cases That Support The Use Of Columnstore Indexes
### Identify Proper Usage Of Clustered And Non-Clustered Columnstore Indexes
### Design Standard Non-Clustered Indexes In Conjunction With Clustered Columnstore Indexes
### Implement Columnstore Index Maintenance

# Implement programmability objects (20–25%)

## Ensure data integrity with constraints

### Define Table And Foreign Key Constraints To Enforce Business Rules
### Write Transact-Sql Statements To Add Constraints To Tables
### Identify Results Of Data Manipulation Language (Dml) Statements Given Existing Tables And Constraints
### Identify Proper Usage Of Primary Key Constraints

## Create stored procedures

### Design Stored Procedure Components And Structure Based On Business Requirements
### Implement Input And Output Parameters
### Implement Table-Valued Parameters
### Implement Return Codes
### Streamline Existing Stored Procedure Logic
### Implement Error Handling And Transaction Control Logic Within Stored Procedures

## Create Triggers And User-Defined Functions

### Design Trigger Logic Based On Business Requirements
### Determine When To Use Data Manipulation Language (Dml) Triggers
### Data Definition Language (Ddl) Triggers
### Or Logon Triggers
### Recognize Results Based On Execution Of After Or Instead Of Triggers
### Design Scalar-Valued And Table-Valued User-Defined Functions Based On Business Requirements
### Identify Differences Between Deterministic And Non-Deterministic Functions

# Manage database concurrency (25–30%)

## Implement transactions

### Identify DML Statement Results Based On Transaction Behavior
### Recognize Differences Between And Identify Usage Of Explicit And Implicit Transactions
### Implement Savepoints Within Transactions
### Determine The Role Of Transactions In High-Concurrency Databases

## Manage isolation levels

### Identify Differences Between Read Uncommitted
### Read Committed
### Repeatable Read
### Serializable
### And Snapshot Isolation Levels
### Define Results Of Concurrent Queries Based On Isolation Level
### Identify The Resource And Performance Impact Of Given Isolation Levels

## Optimize concurrency and locking behavior

### Troubleshoot Locking Issues
### Identify Lock Escalation Behaviors
### Capture And Analyze Deadlock Graphs
### Identify Ways To Remediate Deadlocks

## Implement memory-optimized tables and native stored procedures

### Define Use Cases For Memory-Optimized Tables Versus Traditional Disk-Based Tables
### Optimize Performance Of In-Memory Tables By Changing Durability Settings
### Determine Best Case Usage Scenarios For Natively Compiled Stored Procedures
### Enable Collection Of Execution Statistics For Natively Compiled Stored Procedures

# Optimize database objects and SQL infrastructure (20–25%)

## Optimize statistics and indexes

### Determine The Accuracy Of Statistics And The Associated Impact To Query Plans And Performance
### Design Statistics Maintenance Tasks
### Use Dynamic Management Objects To Review Current Index Usage And Identify Missing Indexes
### Consolidate Overlapping Indexes

## Analyze and troubleshoot query plans

### Capture Query Plans Using Extended Events And Traces
### Identify Poorly Performing Query Plan Operators
### Create Efficient Query Plans Using Query Store
### Compare Estimated And Actual Query Plans And Related Metadata
### Configure Azure Sql Database Performance Insight

## Manage performance for database instances

### Manage Database Workload In Sql Server
### Design And Implement Elastic Scale For Azure Sql Database
### Select An Appropriate Service Tier Or Edition
### Optimize Database File And Tempdb Configuration
### Optimize Memory Configuration
### Monitor And Diagnose Scheduling And Wait Statistics Using Dynamic Management Objects
### Troubleshoot And Analyze Storage, IO, And Cache Issues
### Monitor Azure Sql Database Query Plans

## Monitor and trace SQL Server baseline performance metrics

### Monitor Operating System And Sql Server Performance Metrics
### Compare Baseline Metrics To Observed Metrics While Troubleshooting Performance Issues
### Identify Differences Between Performance Monitoring And Logging Tools, Such As Perfmon And Dynamic Management Objects
### Monitor Azure Sql Database Performance
### Determine Best Practice Use Cases For Extended Events
### Distinguish Between Extended Events Targets
### Compare The Impact Of Extended Events And Sql Trace
### Define Differences Between Extended Events Packages, Targets, Actions, And Sessions



