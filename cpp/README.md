# C/C++ Configuration for FossID-DA

This directory contains a sample configuration file for C/C++ projects that use Conan or CMake.

## Manifest Files
FossID-DA can analyze the following C/C++ manifest files:
- Conan: `conanfile.txt`, `conanfile.py`, `conanfile.lock`
- CMake: `CMakeLists.txt`, `*.cmake`

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type (critical for C/C++ dependencies)

### Processing Options
- `da_ignore_lock_manifests`: Ignore lock files (conanfile.lock) and use conanfile.txt/conanfile.py
- `da_cpp_import_search`: Detect dependencies from C/C++ includes in source files
- `da_only_unmanaged`: Process only unmanaged dependencies from includes

## Import Detection Feature
When `da_cpp_import_search = true` is set, FossID-DA will analyze C/C++ includes directly from source files:

```cpp
#include "boost/goo.h"  // Detected as: boost - N/A
#include "fmt/goo.h"    // Detected as: fmt - N/A
#include <algorithm>    // Standard library, not flagged
#include <functional>   // Standard library, not flagged
```

Note: Version information is marked as N/A for source imports since it cannot be determined from the include statement alone.

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 