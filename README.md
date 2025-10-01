# Jupiter Node

A minimal Jupiter notebook environment with Python and shell support, built with UV for fast dependency management.

## Features

- 🚀 Fast dependency management with UV
- 📓 Jupyter Notebook and JupyterLab support
- 🐍 Python 3.12+ with scientific computing libraries
- 📊 Pre-installed data science packages (pandas, numpy, matplotlib)
- 🔧 Development tools (pytest, black, ruff)

## Quick Start

### 1. Install Dependencies

```bash
uv sync
```

### 2. Select Kernel

After creating a new `.ipynb` notebook:
1. Click on the kernel selector (top right)
2. Choose the kernel under `.venv/bin` (your UV environment)
3. Now you can run Python and bash commands in your notebook

**Example commands:**
- Python: `print("Hello World!")`
- Bash: `!echo "Hello from bash!"`

## What's Included

### Core Jupiter Stack (Required)
- `jupyter>=1.1.1` - Jupiter core functionality
- `jupyterlab>=4.3.0` - Modern Jupiter interface
- `ipykernel>=6.29.5` - Python kernel for Jupiter
- `notebook>=7.2.0` - Classic Jupiter interface
- `ipywidgets>=8.1.5` - Interactive widgets for Jupiter

### Data Science & Visualization (Optional)
- `matplotlib>=3.9.0` - Plotting and visualization
- `pandas>=2.2.0` - Data manipulation and analysis
- `numpy>=2.0.0` - Numerical computing

### General Python Utilities (Optional)
- `requests>=2.32.3` - HTTP requests (for API calls, web scraping)
- `python-dotenv>=1.0.1` - Environment variables (.env files)
- `pyyaml>=6.0.1` - YAML file parsing
- `click>=8.2.1` - CLI framework (for command-line tools)
- `rich>=14.0.0` - Rich text formatting and progress bars

### Development Tools (Optional)
- `pytest>=8.0.0` - Testing framework
- `black>=24.0.0` - Code formatter
- `ruff>=0.11.0` - Fast linter

## Project Structure

```
jupiternode/
├── pyproject.toml      # Project configuration and dependencies
├── .gitignore         # Git ignore rules
├── demo.ipynb         # Demo notebook with Python & bash examples
└── README.md          # This file
```

## Requirements

- Python 3.12 or higher
- UV package manager

## Install UV

If you don't have UV installed:

```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"

# Or with pip
pip install uv
```

## Troubleshooting

### Port Already in Use
```bash
uv run jupyter notebook --port 9999
```

### Dependencies Not Found
```bash
uv sync
```

## Contributing

1. Install development dependencies: `uv sync --group dev`
2. Format code: `uv run black .`
3. Lint code: `uv run ruff check .`
4. Run tests: `uv run pytest`

## License

MIT License
