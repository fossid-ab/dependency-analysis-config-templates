# Go Configuration for FossID-DA

This directory contains a sample configuration file for Go projects that use Go Modules, Dep, Glide, or Godep.

## Manifest Files
FossID-DA can analyze the following Go manifest files:
- GoMod: `go.mod`, `go.sum`
- Dep (legacy): `Gopkg.toml`, `Gopkg.lock`, `godeps`
- Glide (legacy): `glide.lock`
- Godep (legacy): `godeps.json`

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type (important for platform-specific code)
  Affects build tags and conditional imports (// +build linux)
- `da_git_user`: GitHub username for API requests (RECOMMENDED: Define in global FossID configuration to minimize security risks)
- `da_git_token`: GitHub token for API requests (RECOMMENDED: Define in global FossID configuration to minimize security risks)

### Processing Options
- `da_ignore_lock_manifests`: If 0, uses lock files (go.sum) when available
  If 1, ignores lock files and uses go.mod
- `da_go_import_search`: Detect dependencies from Go imports in source files
  Set to 1 to analyze imports in .go files
- `da_only_unmanaged`: Process only unmanaged dependencies from imports
  Applies when da_go_import_search=1

### Dependency Scopes
- `da_ds_test_dependencies`: Process Testing packages like testify, ginkgo, assert frameworks
- `da_ds_dev_dependencies`: Process development tools like golint, gofmt, staticcheck, govulncheck
- `da_ds_optional_dependencies`: Process optional dependencies with build constraints (// +build tags) or optional features
- `da_ds_indirect_dependencies`: Process indirect/transitive dependencies
  Dependencies marked with // indirect comment in go.mod

### Dependency Tree Depth
- `da_gd_go`: Maximum depth for the dependency tree traversal (2 is the default)

## Import Detection Feature
When `da_go_import_search = true` is set, FossID-DA will analyze Go imports directly from source files:

```go
import "github.com/sirupsen/logrus"          // Detected as: sirupsen/logrus - N/A
import "github.com/rs/cors"                  // Detected as: rs/cors - N/A
import "os"                                  // Standard library, not flagged
import "syscall"                             // Standard library, not flagged
```

Note: Version information is marked as N/A for source imports since it cannot be determined from the import statement alone.

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 