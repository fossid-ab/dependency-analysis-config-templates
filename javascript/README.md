# JavaScript/Node.js Configuration for FossID-DA

This directory contains a sample configuration file for JavaScript/Node.js projects that use NPM, Yarn, PNPM, or Bower.

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type - critical for native modules (node-gyp based packages)
  Affects binary/compiled dependencies like sqlite3, canvas, sharp, etc.
- `da_npm_version`: NPM version to use for dependency resolution
  Affects resolution strategy, package-lock.json format, and engine constraints
- `da_node_version`: Node.js version for resolution
  Affects compatibility with packages that specify "engines.node" restrictions

### Processing Options
- `da_use_yarn`: Set to 1 if your project uses Yarn's resolution algorithm (relevant for monorepos)
- `da_allow_node_modules_processing`: Set to 1 to process nested package.json files (increases scan time)
- `da_ignore_lock_manifests`: If 1, ignores lock files and uses package.json

### Dependency Scopes
- `da_ds_peer_dependencies`: Process "peerDependencies" in package.json. Usually libraries like React, webpack plugins - dependencies expected to be provided.
- `da_ds_dev_dependencies`: Process "devDependencies" in package.json. Usually Build tools, test frameworks, linters (eslint, jest, webpack, etc.)
- `da_ds_optional_dependencies`: Process "optionalDependencies" in package.json. Usually packages that enhance functionality but aren't required (chalk, debug, etc.)

### Dependency Tree Depth
- `da_gd_npm`: Maximum depth for dependency tree traversal (10 default). Set to 0 for direct dependencies only 