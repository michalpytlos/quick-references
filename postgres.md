# PostgreSQL - quick reference

## Contents
- [Performance](#performance)
    - [Commands](#commands)
    - [Queries with LIKE](#queries-with-like)
- [Settings](#settings)

## Performance

### Commands
| Command | description | usage |
| ------------| ----------- | --------- |
|[ANALYZE](https://www.postgresql.org/docs/current/sql-analyze.html)|collect statistics about the contents of tables in the database, and store the results in the pg_statistic system catalog|`ANALYZE [ VERBOSE ] [ table_and_columns [, ...] ]`|
|[EXPLAIN](https://www.postgresql.org/docs/current/sql-explain.html)|show the execution plan of a statement|`EXPLAIN [ ( option [, ...] ) ] statement`|
|[VACUUM](https://www.postgresql.org/docs/current/sql-vacuum.html)|garbage-collect and optionally analyze a database|`VACUUM [ ( option [, ...] ) ] [ table_and_columns [, ...] ]`|

### Queries with LIKE
Create trigram index for queries with `LIKE`:
1. Load the pg_trgm extension: `CREATE EXTENSION pg_trgm`
1. Create index: `CREATE INDEX index_name ON table_name USING GIN (column_name gin_trgm_ops)`

[pg_trgm](https://www.postgresql.org/docs/current/pgtrgm.html) provides operator classes for [GIN and GiST](https://www.postgresql.org/docs/current/textsearch-indexes.html) trigram indexes.

## Settings
| Command | description | usage |
| ------------| ----------- | --------- |
|[ALTER SYSTEM](https://www.postgresql.org/docs/current/sql-altersystem.html)|change a server configuration parameter|`ALTER SYSTEM SET configuration_parameter { TO \| = } { value \| 'value' \| DEFAULT }`|
|||`ALTER SYSTEM RESET { configuration_parameter \| ALL } `|
|[SHOW](https://www.postgresql.org/docs/current/sql-show.html)|display the current setting of run-time parameters|`SHOW  { name \| ALL }`|
|[SET](https://www.postgresql.org/docs/current/sql-set.html)|change run-time configuration parameter used by the current session|`SET [ SESSION \| LOCAL ] configuration_parameter { TO \| = } { value \| 'value' \| DEFAULT }`|
