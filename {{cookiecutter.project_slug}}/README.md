# {{cookiecutter.project_slug}}

This template is set up using the new PEP 518 scheme. `pyproject.toml` should contain all Python configuration and eventually
replace `setup.py`, `setup.cfg`, `MANIFEST.in`, `requirements.txt` and the like. Unfortunately, not all Python developer
tools support the new standard, which is why some configuration is still in `setup.cfg`. This file should be removed in
the future.

## Features

### Package manager
This template uses [`poetry`](https://python-poetry.org/) as package manager. This package manager utilizes the new
`pyproject.toml` file and offers similar capabilities to package managers in other languages (npm, cargo, etc.).

### Formatting

#### reorder_python_imports
`reorder_python_imports` enforces a consistent `import` style and is more comprehensive than `isort`.

* bandit
* black 
* mypy/pytypes
* flake8
* pytest
* pycharm integration
* git integration (pre-commit)
  * some hooks from https://github.com/pre-commit/pre-commit-hooks
* bandit
* editorconfig.org
* pyupgrade
* reorder-python-imports

### Pre-commit hooks
Most development tools are executed as pre-commit hooks. These pre-commit hooks are managed using
https://pre-commit.com.

Install pre commit hooks:

`pre-commit install`

It might be necessary to update the pre-commit repos using:

`pre-commit autoupdate`


### CI
Style should be enforced using CI (build should fail if linting fails).
