# Rust/Cargo Configuration for FossID-DA

This directory contains a sample configuration file for Rust projects that use Cargo.

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system setting (corresponds to Rust's target-specific dependencies)
  Affects conditional dependencies with [target.'cfg(unix)'.dependencies]

### Processing Options
- `da_ignore_lock_manifests`: If 0, uses lock files (Cargo.lock) when available
  If 1, ignores lock files and uses Cargo.toml

### Dependency Scopes
- `da_ds_test_dependencies`: Process Dependencies in [dev-dependencies] used in #[cfg(test)]
- `da_ds_dev_dependencies`: Process Development tools in [dev-dependencies] like clippy, rustfmt
- `da_ds_optional_dependencies`: Process Features declared with [features] and optional = true

### Dependency Tree Depth
- `da_gd_cargo`: Maximum depth for the dependency tree traversal (4 is the default)