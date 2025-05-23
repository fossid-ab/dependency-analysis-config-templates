# Ruby Configuration for FossID-DA

This directory contains a sample configuration file for Ruby projects that use Bundler or Gem.

## Key Configuration Options

### Environment Settings
- `da_ruby_version`: Ruby version to use for dependency resolution (default: 3.2.2)
- `da_gem_version`: Gem version to use for resolution (default: 3.0.3)

### Processing Options
- `da_ignore_lock_manifests`: If 0, uses lock files (Gemfile.lock) when available
  If 1, ignores lock files and uses manifests

### Dependency Scopes
- `da_ds_test_dependencies`: Process test groups in Gemfile
  Controls processing of test groups in Gemfile (e.g., group :test)
- `da_ds_dev_dependencies`: Process development groups in Gemfile
  Controls processing of development groups in Gemfile (e.g., group :development)
- `da_ds_optional_dependencies`: Process optional groups in Gemfile
  Controls processing of optional groups in Gemfile

### Dependency Tree Depth
- `da_gd_gem`: Maximum depth for the dependency tree traversal (7 is the default)