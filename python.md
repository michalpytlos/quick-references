# Python - quick reference

## Table of contents
- [Tooling](#tooling)
- [Poetry](#poetry)
- [Useful links](#useful-links)

## Tooling

| tool | description | reference |
| ---- |------------ | -------- |
|IPython|Interactive shell for Python|[docs](https://ipython.readthedocs.io/en/stable/interactive/index.html), [Magic commands](https://ipython.readthedocs.io/en/stable/interactive/magics.html)|
|ipdb|Enhanced pdb|[tutorial](https://www.digitalocean.com/community/tutorials/how-to-use-the-python-debugger)|
|debugpy|Debugger|[github](https://github.com/microsoft/debugpy), [usage with Docker](https://blog.theodo.com/2020/05/debug-flask-vscode/)|
|pipx|Install and run Python applications in isolated environments|[docs](https://pipxproject.github.io/pipx/)|
|Poetry|Packaging tool|[docs](https://python-poetry.org/docs/cli/)|
|Black|Code formatter|[docs](https://black.readthedocs.io/en/stable/), [github](https://github.com/psf/black)|
|isort|Sort imports|[docs](https://pycqa.github.io/isort/)|
|Flake8|Code linter|[man page](https://flake8.pycqa.org/en/latest/manpage.html), [error codes](https://flake8.pycqa.org/en/latest/user/error-codes.html)|
|mypy|Static type checker|[project page](http://mypy-lang.org/)|
|pytest|Testing framework|[docs](https://docs.pytest.org/en/stable/), [tutorial](https://realpython.com/pytest-python-testing/)|
|pytest-cov|Integrate [coverage.py](https://coverage.readthedocs.io/) into pytest|[docs](https://pytest-cov.readthedocs.io/en/latest/readme.html)|
|tox|Testing wrapper|[docs](https://tox.readthedocs.io/en/latest/), [tutorial](https://waprin.io/2015/05/21/introducing-tox.html)|
|pre-commit|Manage pre-commit hooks|[docs](https://pre-commit.com/#intro), [supported hooks](https://pre-commit.com/hooks.html)|
|Cookiecutter|Create projects from project templates|[github](https://github.com/cookiecutter/cookiecutter), [template for Python package](https://github.com/audreyfeldroy/cookiecutter-pypackage)|
|Alembic|Database migration tool|[tutorial](https://alembic.sqlalchemy.org/en/latest/tutorial.html), [create migration script](https://alembic.sqlalchemy.org/en/latest/tutorial.html#create-a-migration-script)|

## Poetry
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

## Useful links
1. [The Python Standard Library](https://docs.python.org/3/library/index.html)
2. [The Python Tutorial](https://docs.python.org/3/tutorial/)
3. [Performance tips](https://wiki.python.org/moin/PythonSpeed/PerformanceTips)
4. [Full Stack Python](https://www.fullstackpython.com/)
5. [The Hitchhiker’s Guide to Python](https://docs.python-guide.org/)
6. [Exploring and understanding Python through surprising snippets](https://github.com/satwikkansal/wtfpython)
7. [Common Python Data Structures (Guide)](https://realpython.com/python-data-structures/)
8. [List of lists of interview questions](https://github.com/MaximAbramchuck/awesome-interview-questions#python)
9. [How to set up Python project](https://sourcery.ai/blog/python-best-practices/)
10. [Python project checklist](http://michal.karzynski.pl/blog/2019/05/26/python-project-maturity-checklist/)
11. [Packaging Python projects](https://packaging.python.org/tutorials/packaging-projects/)
