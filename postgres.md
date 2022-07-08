# PostgreSQL - quick reference

## Contents
- [Performance](#performance)
    - [Commands](#commands)
    - [Queries with LIKE](#queries-with-like)
- [Settings](#settings)
- [Roles and privileges](#roles-and-privileges)
- [Misc.](#miscellaneous)

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

## Miscellaneous
* Use [escape strings](https://www.postgresql.org/docs/current/sql-syntax-lexical.html#SQL-SYNTAX-CONSTANTS) for strings with non-printable characters e.g. `E'\001'` is start of header (SOH) using [ASCII octal](https://web.cs.dal.ca/~zyu/ascii.html) encoding.