# Yocto Configuration for FossID-DA

This directory contains a sample configuration file for Yocto Project and BitBake systems.

## Key Configuration Options

### System Settings
- `da_os_type`: Operating system type for dependency resolution

### Scanning Options
- `da_single_dependency_versions`: Use single dependency version in tree
- `da_ignore_hidden_files`: Ignore hidden files from being processed

### Dependency Scopes
- `da_ds_test_dependencies`: Process dependencies for test packages
- `da_ds_optional_dependencies`: Process optional dependencies (RRECOMMENDS)

### Dependency Tree Depth
- `da_gd_general`: Maximum depth for the dependency tree traversal (4 is the default)