# JavaScript/Node.js Configuration for FossID-DA

This directory contains a sample configuration file for JavaScript/Node.js projects that use NPM, Yarn, PNPM, or Bower.

## Manifest Files
FossID-DA can analyze the following JavaScript manifest files:
- `package.json`: Contains project metadata and dependencies
- `package-lock.json`: NPM lock file specifying exact dependency versions
- `yarn.lock`: Yarn lock file
- `pnpm-lock.yaml`: PNPM lock file
- `bower.json`: Bower package manager configuration (legacy)

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type (important for native Node modules)
- `da_npm_version`: NPM version to use for dependency resolution
- `da_node_version`: Node.js version for resolution
- `da_use_yarn`: Use Yarn instead of NPM for resolution

### Processing Options
- `da_allow_node_modules_processing`: Process manifests inside node_modules folders
- `da_ignore_lock_manifests`: Ignore lock files and use only package.json

### Dependency Scopes
- `da_ds_peer_dependencies`: Process "peerDependencies" in package.json
- `da_ds_dev_dependencies`: Process "devDependencies" in package.json 
- `da_ds_optional_dependencies`: Process "optionalDependencies" in package.json

### Dependency Tree Depth
- `da_gd_npm`: Maximum depth for the dependency tree traversal (0 = direct dependencies only)

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 