# Blank Python Project Template

Minimal Python project template with modern tooling: UV, Black, Ruff, Mypy, Pytest.

## Quick Start

```bash
git clone https://github.com/YOUR_USERNAME/blank.git my-project
cd my-project
make install
make run
```

Edit `src/blank/main.py` to get started.

## Prerequisites

```bash
# Install pyenv and Python 3.13
brew install pyenv
pyenv install 3.13
pyenv global 3.13

# Install UV
brew install uv
```

## Development Commands

```bash
make install       # Install/update dependencies
make run          # Run the application
make lint         # Check code with ruff
make format       # Auto-format code with black
make typecheck    # Type check with mypy
make test         # Run tests with pytest
make check-all    # Run all checks
make clean        # Remove cache files
```

## Project Structure

```
blank/
├── src/blank/           # Your application code
│   ├── __init__.py
│   └── main.py          # Entry point
├── tests/               # Test suite
│   └── test_main.py
├── pyproject.toml       # Project config & dependencies
├── Makefile             # Development commands
├── .python-version      # Python version
└── uv.lock             # Locked dependencies
```

## Renaming the Project

```bash
# Rename to "myapp"
mv src/blank src/myapp

# Update pyproject.toml:
#   name = "myapp"
#   myapp = "myapp.main:main"

make install
uv run myapp
```

## Adding Dependencies

Edit `pyproject.toml`:

```toml
dependencies = [
    "requests>=2.31.0",
]
```

Then run `make install`.

## License

MIT
