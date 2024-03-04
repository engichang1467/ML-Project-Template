# ML Project Setup Template

This is a template for setting up a new machine learning project. It includes automation features to make sure our code style is clean and unit testing.

So here is our set of tools to set up:

- `poetry`: Sort out virtual environments for good, all your project definitions in `pyproject.toml`.
- `black`: You can have any code style until it is black. Stop worrying about formatting your code.
- `ruff`: New blazing fast linter, anything that black doesn't care about will be fixed here.
- `pytest`: To unit test your code.
- `pre-commit-hooks`: Automate all of the above and forget about them.
- `GitHub Actions`: Run these on the remote as well, just to be sure.

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

Feel free to create your own python scripts and run them using the following command:

```bash
poetry run python <python_script.py>
```

## References

- [CQ4DS - Python project from scratch with poetry, black, ruff, pytest, pre-commit-hooks and GitHub Actions in 15 minute tops](https://laszlo.substack.com/p/cq4ds-python-project-from-scratch)
