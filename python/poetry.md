# Poetry CLI

Selected commands

| Command | description | usage |
| ------- | ----------- | ----- |
|add|Add new dependency to pyproject.toml|`poetry add [OPTIONS] PACKAGE [PACKAGE...]`|
||Add as dev dependency|`--dev`|
||Dry run|`--dry-run`|
|check|Validate pyproject.toml|`check`|
|config|Edit config|`poetry config [OPTIONS] [KEY] [VALUE] [KEY...] [VALUE...]`|
||List config settings|`--list`|
|env|Manage virtualenvs|`env SUBCOMMAND`|
||Display info about current environment|`env info [--path]`|
||List all virtualenvs associated with current project|`env list [--full-path]`|
||Remove virtualenv associated with project|`env remove PYTHON_EXECUTABLE`|
||Activate or create new virtualenv for current project|`env use PYTHON_EXECUTABLE`|
|init|Create pyproject.toml file in current dir|`init [OPTIONS]`|
|install|Download and install dependecies from lock file. If lock file is not present, use pyproject.toml.|`install [OPTIONS]`|
||Do not install dev dependecies|`--no-dev`|
||Dry run|`--dry-run`|
||Remove packages not present in lock file|`--remove-untracked`|
|lock|Process pyproject.toml and lock dependencies in lock file|`lock [--no-update]`|
|remove|Remove dependency from pyproject.toml and lock file|`remove [OPTIONS] PACKAGE [PACKAGE...]`|
||Remove package from dev dependencies|`--dev`|
||Do not remove package from pyproject.toml|`--dry-run`|
|search|Search for package on remote index|`search PACKAGE [PACKAGE...]`|
|show|Display detailed info about package or list all installed packages|`show [OPTIONS] [PACKAGE]`|
||List dependencies as tree|`-t, --tree`|
||Show latest versions for packages that are outdated|`-o, --outdated`|
|update|Get latest versions of dependencies and update lock file|`update [OPTIONS] [PACKAGE] [PACKAGE...]`|
||Only update lock file|`--lock`|

Reference: [CLI docs](https://python-poetry.org/docs/cli/)