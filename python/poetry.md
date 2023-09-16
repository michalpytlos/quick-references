# Poetry CLI

## Contents
- [CLI](#selected-commands)
- [Version constraints](#version-constraints)
- [Env with custom Python version](#env-with-custom-python-version)

## Selected commands

| Command | description | usage |
| ------- | ----------- | ----- |
|[add](https://python-poetry.org/docs/cli/#add)|Add new dependency to pyproject.toml|`poetry add [OPTIONS] PACKAGE[@VERSION_CONSTRAINT] [PACKAGE...]`|
||Add as dev dependency|`--dev`|
||Dry run|`--dry-run`|
|check|Validate pyproject.toml|`poetry check`|
|config|Edit config|`poetry config [OPTIONS] [KEY] [VALUE] [KEY...] [VALUE...]`|
||List config settings|`--list`|
|[env](https://python-poetry.org/docs/managing-environments/)|Manage virtualenvs|`poetry env SUBCOMMAND`|
||Display info about current environment|`env info [--path]`|
||List all virtualenvs associated with current project|`env list [--full-path]`|
||Remove virtualenv associated with project|`env remove PYTHON_EXECUTABLE`|
||Activate or create new virtualenv for current project|`env use PYTHON_EXECUTABLE`|
|init|Create pyproject.toml file in current dir|`poetry init [OPTIONS]`|
|[install](https://python-poetry.org/docs/cli/#install)|Download and install dependecies from lock file. If lock file is not present, use pyproject.toml.|`poetry install [OPTIONS]`|
||Synchronize environment with lock file|`--sync`|
||Do not install current project|`--no-root`|
||Do not install dev dependecies|`--no-dev`|
||Dry run|`--dry-run`|
||Remove packages not present in lock file|`--remove-untracked`|
|lock|Process pyproject.toml and lock dependencies in lock file|`poetry lock [--no-update]`|
|remove|Remove dependency from pyproject.toml and lock file|`poetry remove [OPTIONS] PACKAGE [PACKAGE...]`|
||Remove package from dev dependencies|`--dev`|
||Do not remove package from pyproject.toml|`--dry-run`|
|search|Search for package on remote index|`poetry search PACKAGE [PACKAGE...]`|
|shell|Spawn shell within virtual environment|`poetry shell`|
|[show](https://python-poetry.org/docs/cli/#show)|Display detailed info about package or list all installed packages|`poetry show [OPTIONS] [PACKAGE]`|
||List dependencies as tree|`-t, --tree`|
||Show latest versions for packages that are outdated|`-o, --outdated`|
|[update](https://python-poetry.org/docs/cli/#update)|Get latest versions of dependencies and update lock file|`poetry update [OPTIONS] [PACKAGE] [PACKAGE...]`|
||Only update lock file|`--lock`|
|[version](https://python-poetry.org/docs/master/cli/#version)|Show or bump version of project|`poetry version [ major \| minor \| patch ]`|

Reference: [CLI docs](https://python-poetry.org/docs/cli/)

## Version constraints
| Example | Description | Operator doc |
| -------- | ----------- | -------- |
|`^1.2.3`|Allow for minor- and patch-level updates|[caret](https://python-poetry.org/docs/dependency-specification/#caret-requirements)|
|`~1.2.3`|Allow for patch-level updates|[tilde](https://python-poetry.org/docs/dependency-specification/#tilde-requirements)|
|`1.2.*`|Allow for latest where wildcard is positioned|[wildcard](https://python-poetry.org/docs/dependency-specification/#wildcard-requirements)|

## Env with custom Python version

1. Set Python version in the current terminal session: `pyenv shell <version>`
1. Create env: `pyenv which python | xargs poetry env use`

