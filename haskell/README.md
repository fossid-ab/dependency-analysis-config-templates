# Haskell Configuration for FossID-DA

This directory contains a sample configuration file for Haskell projects that use Cabal or Stack.

## Key Configuration Options

### System Settings
- `da_os_type`: Operating system type for dependency resolution

### Scanning Options
- `da_ignore_lock_manifests`: Ignore lock files and use project files
- `da_single_dependency_versions`: Use single dependency version in tree
- `da_ignore_hidden_files`: Ignore hidden files from being processed

### Dependency Scopes
- `da_ds_test_dependencies`: Process test suites and test dependencies
- `da_ds_dev_dependencies`: Process development dependencies
- `da_ds_optional_dependencies`: Process optional dependencies

### Dependency Tree Depth
- `da_gd_general`: Maximum depth for the dependency tree traversal (4 is the default) 