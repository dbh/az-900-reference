- [Databases](#databases)
  - [Cosmos DB](#cosmos-db)
  - [SQL Database](#sql-database)
  - [Azure DB for MySQL](#azure-db-for-mysql)
  - [Azure DB for PostgreSQL](#azure-db-for-postgresql)
    - [Service tiers](#service-tiers)
    - [Deployment modes](#deployment-modes)
  - [Azure SQL Managed Instance](#azure-sql-managed-instance)
    - [Migration](#migration)
# Databases
* Cosmos DB
* SQL Database
* SQL Managed Instance
* Azure DB for MySQL
* Azure DB for PosgreSQL
* Synapse Analytics
* HDInsight
* Databricks
* Data Lake Analytics

## Cosmos DB

Points
* Devs used different databases and APIs to get at the data
* global distrib
* multi-model db svc
* elastically and independently scale throughput and storage
* SLA options available for
  * throughput
  * latency
  * availability
  * consistency guarantees
* schemaless data
  * support constantly changing data
  * always on
* stores in ARS Atom-record-sequence format
* abstracted/projected as an API
* APIs
  * SQL
  * MongoDB
  * Cassandra
  * Tables
  * Gremlin
* Devs can stick with APIs they know

## SQL Database

Points
* PaaS database engine

Features
* handles most db mgmt functions automatically
  * upgrading 
  * patching
  * backups
  * monitoring
* 99.99 % avail
* fully managed
* high avail
* backups
* all updates to SQL and OS handled
* Uses
  * Relational
  * non-relational structures
    * graph
    * JSON
    * spatial
    * XML
* Easy Migration


## Azure DB for MySQL
* relational (obv)
* mysql community edition (obv)
* pay as you go
* scaling as needed (seconds)
* ability to protect sensitive data rest/in motion
* automatic backups
* enterprise grade sec and compliance
* no Vms
* admin via
  * azure cli
  * azure portal
  * custom mgmt app



## Azure DB for PostgreSQL
* high avail compared to on-prem
* simple/flexible pricing based on tier
* db as a service
* scale up/down as needed. Seconds
* auto backups. Retention 35 days
* ent grad sec. compliance. 
* prot data at rest/in motion
* SSL encryption between client & server

### Service tiers
multiple. diff perf and capabilities
* Basic
* General purpose
* memory optimized

### Deployment modes
* Single Server
  * 99% sla
  * pay as you go
  * verticle scale as needed
  * monitor/alert
* Hyperscale (Citus)
  * horizontal scaling of queries across multi machines by sharding
  * faster for large datasets
  * real-time analytics
  * high throughput ransactional workloads

## Azure SQL Managed Instance

* scalable cloud data service
* broadest sql server compat
* fully managed
* PaaS
* 99.99% uptime SLA
* some features not in "Azure SQL Database"
  * char encoding other than SQL Latin 1 General CP CI AS (Now that's dumb to not include in the other one)


### Migration
Discover -> Assess -> migrate -> Cutover -> Optimize