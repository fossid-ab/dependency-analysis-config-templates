# .NET/C# Configuration for FossID-DA

This directory contains a sample configuration file for .NET/C# projects that use NuGet packages.

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type (important for platform-specific assemblies)
- `da_dotnet_framework`: Target .NET Framework version
- `da_dotnet_standard`: Target .NET Standard version

### Processing Options
- `da_ignore_lock_manifests`: Ignore lock files (packages.lock.json) and use project files

### Dependency Scopes
- `da_ds_test_dependencies`: Process test frameworks like MSTest, NUnit, xUnit, Moq, FluentAssertions
- `da_ds_dev_dependencies`: Process development tools, analyzers, code generators (StyleCop, Roslyn analyzers)
- `da_ds_optional_dependencies`: Process conditional dependencies based on target framework or platform

### Dependency Tree Depth
- `da_gd_general`: Maximum depth for the dependency tree traversal (4 is the default)

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 