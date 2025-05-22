# Bazel Configuration for FossID-DA

This directory contains a sample configuration file for projects that use the Bazel build system.

## Manifest Files
FossID-DA can analyze the following Bazel manifest files:
- `WORKSPACE`: Workspace definition and external dependencies
- `BUILD` files: Build targets and dependencies
- `MODULE.bazel`: Bzlmod dependencies (newer Bazel versions)

## Key Configuration Options

### System Settings
- `da_os_type`: Operating system type for dependency resolution

### Scanning Options
- `da_single_dependency_versions`: Use single dependency version in tree
- `da_ignore_hidden_files`: Ignore hidden files from being processed

### Dependency Scopes
- `da_ds_test_dependencies`: Process dependencies for test targets

### Dependency Tree Depth
- `da_gd_general`: Maximum depth for the dependency tree traversal

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 