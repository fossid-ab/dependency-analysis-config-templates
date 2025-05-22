# Ruby Configuration for FossID-DA

This directory contains a sample configuration file for Ruby projects that use Bundler or Gem.

## Manifest Files
FossID-DA can analyze the following Ruby manifest files:
- Bundler: `Gemfile`, `Gemfile.lock`
- Gem: `*.gemspec`

## Key Configuration Options

### Environment Settings
- `da_ruby_version`: Ruby version to use for dependency resolution
- `da_gem_version`: Gem version to use for resolution

### Processing Options
- `da_ignore_lock_manifests`: Ignore lock files (Gemfile.lock) and use manifests

### Dependency Scopes
- `da_ds_test_dependencies`: Process test groups in Gemfile
- `da_ds_dev_dependencies`: Process development groups in Gemfile
- `da_ds_optional_dependencies`: Process optional groups in Gemfile

### Dependency Tree Depth
- `da_gd_gem`: Maximum depth for the dependency tree traversal

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 