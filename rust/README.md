# Rust/Cargo Configuration for FossID-DA

This directory contains a sample configuration file for Rust projects that use Cargo.

## Manifest Files
FossID-DA can analyze the following Rust manifest files:
- Cargo: `Cargo.toml`, `Cargo.lock`

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type (important for platform-specific features/dependencies)

### Processing Options
- `da_ignore_lock_manifests`: Ignore lock files (Cargo.lock) and use Cargo.toml

### Dependency Scopes
- `da_ds_test_dependencies`: Process dependencies needed for tests
- `da_ds_dev_dependencies`: Process "dev-dependencies" section
- `da_ds_optional_dependencies`: Process optional features

### Dependency Tree Depth
- `da_gd_cargo`: Maximum depth for the dependency tree traversal

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 