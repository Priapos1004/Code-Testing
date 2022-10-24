# Code-Testing

tools for improving your code

## create a virtual environment from testing.yml

```
conda env create --file testing.yml
```

if you want to overwrite an existing environment with the name "testing"

```
conda env create --force --file testing.yml
```

## improve your code

You can run all these commands also recursively that means it will run for all files in all subfolder from your current working directory with replacing `<filename>.py` with `.`.

### isort

[`isort`](https://github.com/PyCQA/isort) is a library to sort imports alphabetically and automatically separate them into sections by type. You can run it for one file:

```
isort <filename>.py
```

### black

[`black`](https://github.com/psf/black) is the uncompromising Python code formatter. It deletes unnecessary whitespaces and formats your lists, dictionaries, and similar datatypes. You can run this for one file with:

```
black <filename>.py
```

**NOTE:** be aware that sometimes the result can look less readable

### flake8

[`flake8`](https://flake8.pycqa.org/en/latest/) is a tool for style guide enforcement. It outputs you the lines in the script that have an unclean style and how to clean them up. You can run this for one file with:

```
flake8 <filename>.py
```

### mypy

[`mypy`](https://github.com/python/mypy) is a tool for type checking (similar to flake8 for style). It outputs missing or wrong type hints. You can run this for one file with:

```
mypy <filename>.py
```

### refurb

[`refurb`](https://github.com/dosisod/refurb) is a tool for modernizing Python codebases. It outputs hints for optimizing your code. You can run this for one file with:

```
refurb <filename>.py
```

### pytest

[`pytest`](https://docs.pytest.org/) is tool for writing small and readable tests for your code. You can run this with:

```
pytest
```

## check your code with github workflow

create in your repository the folder structure `.github/workflows` and add there `code_quality.yml` to check your code quality after every push.
