# Python project template

A simply python template including black, isort, flake8, and mypy.

Search for `<project-name>` for spots where you need to substitue your own project name. You should also change the
`author` field in `pyproject.toml`.

It may also be useful to update tool versions in `pyproject.toml` and `.pre-commit-config.yaml`.

## Setup

1. Set up python:
   - Install [`pyenv`](https://github.com/pyenv/pyenv) and
     [`pyenv-virtualenv`](https://github.com/pyenv/pyenv-virtualenv)
   - Run `cat pyproject.toml` to find the desired python version. It will look like `python = "^<version>"`
   - Run `pyenv versions` to see if a matching python version is installed. If not, run `pyenv install <version>` to
     install a matching version.
   - Run `pyenv virtualenv <version> <project-name>` to create a new virtualenv for this project (`version` must
     be a full `vX.X.X`, not just a `vX.X`)
   - Run `pyenv local <project-name>` to assign the virtualenv to this directory (by creating a `.python-version`
     file)
2. Install dependencies:
   - Install [`poetry`](https://python-poetry.org/) using [`pipx`](https://pipx.pypa.io/stable/):
     `pipx install poetry`
   - Run `poetry install --no-root` to install python dependencies from `pyproject.toml`
3. Set up pre-commit:
   - Install [`pre-commit`](https://pre-commit.com/) using [`pipx`](https://pipx.pypa.io/stable/):
     `pipx install pre-commit`
   - Run `pre-commit install` to activate pre-commit hooks for this repo

## Running

`python main.py`
