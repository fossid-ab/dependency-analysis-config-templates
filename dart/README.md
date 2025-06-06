# Dart/Flutter Configuration for FossID-DA

This directory contains a sample configuration file for Dart and Flutter projects that use Pub.

## Key Configuration Options

### System Settings
- `da_os_type`: Operating system type for dependency resolution
  - Options: win32, win64, darwin, debian, unix
  - Set to "unix" for cross-platform compatibility

### Processing Options
- `da_ignore_lock_manifests`: Controls lock file handling
  - 0: Use lock files (pubspec.lock) when available (default)
  - 1: Ignore lock files and use pubspec.yaml

### Dependency Scopes
- `da_ds_dependency_overrides`: Process "dependency_overrides" section in pubspec.yaml
  - Used for overriding specific dependency versions
- `da_ds_dev_dependencies`: Process "dev_dependencies" section in pubspec.yaml
  - These are dependencies only needed during development (testing, linting, etc.)

### Dependency Tree Depth
- `da_gd_general`: Maximum depth for the dependency tree traversal (default: 4)

### Ignore Settings
- `da_ignore_folders`: Folders to ignore during analysis
  - Default: "" (no folders ignored)
  - Can be set to ignore build artifacts, caches, etc. 