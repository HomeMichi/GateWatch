<!-- CI -->

[![CI](https://github.com/HomeMichi/GateWatch/actions/workflows/ci.yml/badge.svg)](https://github.com/HomeMichi/GateWatch/actions/workflows/ci.yml)

<!-- Coverage (Codecov or Coveralls – pick one) -->

[![codecov](https://img.shields.io/codecov/c/github/HomeMichi/GateWatch.svg)](https://app.codecov.io/gh/HomeMichi/GateWatch)

[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/HomeMichi/GateWatch/main.svg)](https://results.pre-commit.ci/latest/github/HomeMichi/GateWatch/main)

## About

-

## Installation

### 1. Prerequisites

This project uses `uv` for package and environment management

**Install `uv`:**

- **macOS / Linux:**
  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```
- **Windows (PowerShell):**
  ```powershell
  irm https://astral.sh/uv/install.ps1 | iex
  ```

### 2. Initial Project Setup

These commands will set up your virtual environment, install dependencies, and enable automated quality checks.

```bash
# 1. Create a virtual environment in a .venv directory
uv venv

# 2. Activate the virtual environment
#    macOS / Linux
source .venv/bin/activate
#    Windows (PowerShell)
.venv\Scripts\Activate.ps1

# 3. Install all dependencies in "editable" mode
uv pip install -e ".[dev]"

# 4. Install the pre-commit hooks for automated quality checks
pre-commit install
```

### 3. VSCode Integration

To get the best experience (live error-checking, auto-formatting), configure VSCode to use the project's environment.

1.  **Install Recommended Extensions:**

    - `Python` (by Microsoft)
    - `Ruff` (by Astral)
    - `Mypy Type Checker` (by Microsoft)

2.  **Select the Python Interpreter:**
    - Open the Command Palette: `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac).
    - Run the **`Python: Select Interpreter`** command.
    - Choose the interpreter located in the `./.venv` directory. This is critical for all editor integrations to work.

Once the interpreter is selected, our project's `.vscode/settings.json` file will automatically enable formatting on save, import sorting, and type-checking.

### 4. Running Tests

To run the full test suite, simply use `pytest`:

```bash
pytest
```

If you run into "command not found" for `pytest`, install dev requirements first in your project's virtualenv:

PowerShell:

```powershell
.venv\Scripts\Activate.ps1
uv pip install -e ".[dev]"
pytest -q
```

### 5. Formatting and Linting

- If you want to invoke the pre-commit formatting and type-checking explicitly, activate the environment and run

```bash

pre-commit run --all-files
# For ruff hecks only
ruff check .
ruff format
# For MyPy static type checking only
mypy .
```

### Semantic Versioning

- ...

## Temp

- pyproject.toml: all configuration about the project
- uv: packet manager
- mypy: static type checking
- ruff: code formating etc.
- Github actions for CI

---

- Shields.io for README badges
- pydantic for runtime data validation
- dynamic versioning via git tags
-
