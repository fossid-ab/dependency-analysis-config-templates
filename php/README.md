# PHP/Composer Configuration for FossID-DA

This directory contains a sample configuration file for PHP projects that use Composer.

## Key Configuration Options

### Processing Options
- `da_ignore_lock_manifests`: Ignore lock files (composer.lock) and use composer.json

### Dependency Scopes
- `da_ds_ext_dependencies`: Process PHP extension dependencies like ext-curl, ext-json
- `da_ds_test_dependencies`: Process test packages in require-dev
- `da_ds_dev_dependencies`: Process "require-dev" section
- `da_ds_optional_dependencies`: Process "suggest" section

## Extension Dependencies
When `da_ds_ext_dependencies = true` is set, FossID-DA will add information about the ext-{package} dependencies from composer.json manifests:

```
"ext-curl": "*" ==> php-curl  
"ext-json": "*" ==> php-json
```

### Dependency Tree Depth
- `da_gd_general`: Maximum depth for the dependency tree traversal (4 is the default)

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 