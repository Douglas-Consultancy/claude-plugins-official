# Conda Python Dev Plugin

A Claude Code plugin for Python development workflows using Conda. Provides three commands to set up your environment, lint your code, and run your tests — all within a Conda-managed environment.

## Commands

### `/conda-python-dev:conda-setup`

Set up or update your Conda Python environment from `environment.yml`.

```
/conda-python-dev:conda-setup
/conda-python-dev:conda-setup my-env-name
```

### `/conda-python-dev:conda-lint`

Lint Python source code using flake8. Runs a strict pass first (syntax errors, undefined names), then a full warning pass.

```
/conda-python-dev:conda-lint
/conda-python-dev:conda-lint src/mymodule.py
```

### `/conda-python-dev:conda-test`

Run the pytest test suite inside the Conda environment.

```
/conda-python-dev:conda-test
/conda-python-dev:conda-test tests/test_api.py -v
```

## Prerequisites

- [Conda](https://docs.conda.io/en/latest/) installed and available on your PATH
- An `environment.yml` file in your project root (required for `conda-setup`)
- Claude Code 1.0.33 or later

## Installation

```
/plugin install conda-python-dev
```

Or load locally during development:

```
claude --plugin-dir ./plugins/conda-python-dev
```

## License

Apache 2.0
