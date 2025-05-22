# Python Configuration for FossID-DA

This directory contains a sample configuration file for Python projects that use PIP, Pipenv, Poetry, or Hatch.

## Manifest Files
FossID-DA can analyze the following Python manifest files:
- PIP: `requirements.txt`, `setup.py`, `METADATA`
- Pipenv: `Pipfile`, `Pipfile.lock`
- Poetry: `pyproject.toml`, `poetry.lock` (only lock files are processed)
- Hatch: `pyproject.toml`, `hatch.toml`

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type (important for platform-specific wheels)
- `da_python_version`: Python version to use for dependency resolution

### Processing Options
- `da_ignore_lock_manifests`: Ignore lock files (Pipfile.lock, poetry.lock) and use manifests
- `da_py_import_search`: Detect dependencies from Python imports in source files
- `da_only_unmanaged`: Process only unmanaged dependencies from imports

### Dependency Scopes
- `da_ds_hatch_envs`: Comma-separated Hatch environments to process (e.g., "default,lint")
- `da_ds_test_dependencies`: Process "tests_require" or test extras
- `da_ds_dev_dependencies`: Process development extras
- `da_ds_optional_dependencies`: Process "extras_require" groups

### Dependency Tree Depth
- `da_gd_pypi`: Maximum depth for the dependency tree traversal

## Import Detection Feature
When `da_py_import_search = true` is set, FossID-DA will analyze Python imports directly from source files:

```python
import imgviz    # Detected as: imgviz - N/A
import torch     # Detected as: torch - N/A
import math      # Standard library, not flagged
import os        # Standard library, not flagged
```

Note: Version information is marked as N/A for source imports since it cannot be determined from the import statement alone.

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 