# Python Configuration for FossID-DA

This directory contains a sample configuration file for Python projects that use PIP, Pipenv, Poetry, or Hatch.

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type - affects binary wheel selection and platform-specific dependencies
  Determines which wheels are selected (e.g., manylinux vs win32)
- `da_python_version`: Python version to use for dependency resolution
  Affects compatibility checks and version-specific package variants

### Processing Options
- `da_ignore_lock_manifests`: If 0, uses lock files (Pipfile.lock, poetry.lock) when available
  If 1, ignores lock files and uses manifests
- `da_py_import_search`: Detect dependencies from Python imports in source files
  Analyzes "import" and "from ... import" statements in source code
- `da_only_unmanaged`: Process only unmanaged dependencies from imports
  Applies when da_py_import_search=1

### Dependency Scopes
- `da_ds_hatch_envs`: Comma-separated Hatch environments to process (e.g., "default,lint")
- `da_ds_test_dependencies`: Process "tests_require" or test extras
  pytest, unittest, nose dependencies in "test" extras or tests_require
- `da_ds_dev_dependencies`: Process development extras
  Development tools like black, mypy in "dev" extras
- `da_ds_optional_dependencies`: Process "extras_require" groups
  Optional feature groups specified in extras_require (e.g., [aws], [postgres])

### Dependency Tree Depth
- `da_gd_pypi`: Maximum depth for the dependency tree traversal (3 is the default)

## Import Detection Feature
When `da_py_import_search = true` is set, FossID-DA will analyze Python imports directly from source files:

```python
import imgviz    # Detected as: imgviz - N/A
import torch     # Detected as: torch - N/A
import math      # Standard library, not flagged
import os        # Standard library, not flagged
```

Note: Version information is marked as N/A for source imports since it cannot be determined from the import statement alone.