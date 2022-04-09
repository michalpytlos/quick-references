# Alembic CLI

| Command | description | usage |
| ------- | ----------- | ----- |
|current|Display current revision for database|`alembic current`|
|downgrade|Revert to previous revision|`alembic downgrade [OPTIONS] REVISION`|
|heads|Show current available heads|`alembic heads [OPTIONS]`|
|history|List changeset scripts in chronological order|`alembic history [OPTIONS]`|
|init|Initialize new scripts dir|`alembic init [OPTIONS] DIRECTORY`|
|revision|Create new revision file|`alembic revision [OPTIONS]`|
||Add message to use with revision|`-m MESSAGE`|
||Populate revision script with candidate migration operations|`--autogenerate`|
|show|Show revisions denoted by given symbol|`alembic show [OPTIONS] SHORT_REV_HASH`|
|upgrade|Upgrade to later revision|`alembic upgrade [OPTIONS] REVISION`|

Other commands: `branches | edit | ensure_version | list_templates | merge | stamp`
