# Elixir Configuration for FossID-DA

This directory contains a sample configuration file for Elixir projects that use Mix and Hex package manager.

## Manifest Files
FossID-DA can analyze the following Elixir manifest files:
- `mix.exs`: Project and dependency declarations
- `mix.lock`: Lock file with exact dependency versions

## Key Configuration Options

### System Settings
- `da_os_type`: Operating system type for dependency resolution

### Scanning Options
- `da_ignore_lock_manifests`: Ignore lock files (mix.lock) and use mix.exs
- `da_single_dependency_versions`: Use single dependency version in tree
- `da_ignore_hidden_files`: Ignore hidden files from being processed

### Dependency Scopes
- `da_ds_test_dependencies`: Process dependencies in the `:test` environment
- `da_ds_dev_dependencies`: Process dependencies in the `:dev` environment
- `da_ds_optional_dependencies`: Process optional dependencies

### Dependency Tree Depth
- `da_gd_general`: Maximum depth for the dependency tree traversal

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 