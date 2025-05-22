# Pants Configuration for FossID-DA

This directory contains a sample configuration file for projects that use the Pants build system.

## Manifest Files
FossID-DA can analyze the following Pants manifest files:
- `BUILD` files: Build targets and dependencies
- `pants.toml`: Pants configuration
- `3rdparty/python/requirements.txt`: Python dependencies (common pattern)
- `3rdparty/jvm/BUILD`: JVM dependencies (common pattern)

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