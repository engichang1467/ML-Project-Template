# ML Project Setup Template

This is a template for setting up a new machine learning project. It includes a basic project structure, a Makefile for running common commands, and a Dockerfile for running the project in a container.

## Environment setup

```bash
pip install virtualenv
virtualenv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Once `poetry` is installed, you can install the project dependencies by running:

```bash
poetry add black ruff pytest pre-commit
```

### Set up Pre-commit hooks - automation

- **Note**: Make sure you either fork this repo or create a new repo with the same structure and copy the `.pre-commit-config.yaml` file to the root of your project.

```bash
pre-commit install
```

## Running the project

```bash
poetry run python <python_script.py>
```

## References

- [CQ4DS - Python project from scratch with poetry, black, ruff, pytest, pre-commit-hooks and GitHub Actions in 15 minute tops](https://laszlo.substack.com/p/cq4ds-python-project-from-scratch)
