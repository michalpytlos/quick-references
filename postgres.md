# PostgreSQL - quick reference

## Contents
- [System stats and info](#system-info-and-statistics)
- [Settings](#settings)
- [Roles and privileges](#roles-and-privileges)
- [Performance](#performance)
    - [ANALYZE, EXPLAIN and VACUUM](#analyze-explain-and-vacuum)
    - [Inserting large amount of data](#inserting-large-amount-of-data)
    - [Queries with LIKE](#trigram-index-for-queries-with-like)
- [Misc.](#miscellaneous)

## System stats and info
| Table | description |
| ------| ----------- |
|[pg_stat_activity](https://www.postgresql.org/docs/current/monitoring-stats.html#MONITORING-PG-STAT-ACTIVITY-VIEW)|information about system processes|
|[pg_stat_all_tables](https://www.postgresql.org/docs/current/monitoring-stats.html#MONITORING-PG-STAT-ALL-TABLES-VIEW)|statistics about accesses to each table|
|[pg_stat_database](https://www.postgresql.org/docs/current/monitoring-stats.html#MONITORING-PG-STAT-DATABASE-VIEW)|database-wide statistics for each database|
|[pg_database](https://www.postgresql.org/docs/current/catalog-pg-database.html)|information about the available databases|
|[pg_tables](https://www.postgresql.org/docs/current/view-pg-tables.html)|information about each table in the current database|

## Settings
### Displaying and altering settings
| Command | description | usage |
| ------------| ----------- | --------- |
|[ALTER SYSTEM](https://www.postgresql.org/docs/current/sql-altersystem.html)|change a server configuration parameter|`ALTER SYSTEM SET configuration_parameter { TO \| = } { value \| 'value' \| DEFAULT }`|
|||`ALTER SYSTEM RESET { configuration_parameter \| ALL } `|
|[SHOW](https://www.postgresql.org/docs/current/sql-show.html)|display the current setting of run-time parameters|`SHOW  { name \| ALL }`|
|[SET](https://www.postgresql.org/docs/current/sql-set.html)|change run-time configuration parameter used by the current session|`SET [ SESSION \| LOCAL ] configuration_parameter { TO \| = } { value \| 'value' \| DEFAULT }`|

## Roles and privileges
### Commands
| Command | description | usage |
| ------------| ----------- | --------- |
|[CREATE ROLE](https://www.postgresql.org/docs/current/sql-createrole.html)|define new database role|`CREATE ROLE name [ [ WITH ] option [ ... ] ]`|
|[GRANT](https://www.postgresql.org/docs/current/sql-grant.html)|grant access privileges||
|[REVOKE](https://www.postgresql.org/docs/current/sql-revoke.html)|remove access privileges||

### Information on current access privileges
| Level | Table | Command |
| ----- | ----- | ------- |
|Database|[pg_roles](https://www.postgresql.org/docs/current/view-pg-roles.html)|`SELECT * FROM pg_catalog.pg_roles;`|
|Schema|[pg_namespace](https://www.postgresql.org/docs/current/catalog-pg-namespace.html)|`SELECT * FROM pg_catalog.pg_namespace;`|
|Table|[table_privileges](https://www.postgresql.org/docs/current/infoschema-table-privileges.html)|`SELECT * FROM information_schema.table_privileges;`|
|Column|[column_privileges](https://www.postgresql.org/docs/current/infoschema-column-privileges.html)|`SELECT * FROM information_schema.column_privileges;`|
## Performance
###  ANALYZE, EXPLAIN and VACUUM
| Command | description | usage |
| ------------| ----------- | --------- |
|[ANALYZE](https://www.postgresql.org/docs/current/sql-analyze.html)|collect statistics about the contents of tables in the database, and store the results in the pg_statistic system catalog|`ANALYZE [ VERBOSE ] [ table_and_columns [, ...] ]`|
|[EXPLAIN](https://www.postgresql.org/docs/current/sql-explain.html)|show the execution plan of a statement|`EXPLAIN [ ( option [, ...] ) ] statement`|
|[VACUUM](https://www.postgresql.org/docs/current/sql-vacuum.html)|garbage-collect and optionally analyze a database|`VACUUM [ ( option [, ...] ) ] [ table_and_columns [, ...] ]`|
### Inserting large amount of data
1. [Disable AUTOCOMMIT when using multiple INSERTs](https://www.postgresql.org/docs/current/populate.html#DISABLE-AUTOCOMMIT)
1. [Use COPY instead of series of INSERT commands](https://www.postgresql.org/docs/current/populate.html#POPULATE-COPY-FROM)
1. [Remove indexes](https://www.postgresql.org/docs/current/populate.html#POPULATE-RM-INDEXES)
1. [Remove FK constraints](https://www.postgresql.org/docs/current/populate.html#POPULATE-RM-FKEYS)
1. [Increase maintenance_work_mem](https://www.postgresql.org/docs/current/populate.html#POPULATE-WORK-MEM)
1. [Increase max_wal_size](https://www.postgresql.org/docs/current/populate.html#POPULATE-MAX-WAL-SIZE)
1. [Run ANALYZE afterwards](https://www.postgresql.org/docs/current/populate.html#POPULATE-ANALYZE)
### Trigram index for queries with LIKE
Create trigram index for queries with `LIKE`:
1. Load the pg_trgm extension: `CREATE EXTENSION pg_trgm`
1. Create index: `CREATE INDEX index_name ON table_name USING GIN (column_name gin_trgm_ops)`

[pg_trgm](https://www.postgresql.org/docs/current/pgtrgm.html) provides operator classes for [GIN and GiST](https://www.postgresql.org/docs/current/textsearch-indexes.html) trigram indexes.

## Miscellaneous
* Use [escape strings](https://www.postgresql.org/docs/current/sql-syntax-lexical.html#SQL-SYNTAX-CONSTANTS) for strings with non-printable characters e.g. `E'\001'` is start of header (SOH) using [ASCII octal](https://web.cs.dal.ca/~zyu/ascii.html) encoding.