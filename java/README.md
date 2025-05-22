# Java/Scala/Kotlin Configuration for FossID-DA

This directory contains a sample configuration file for Java, Scala, and Kotlin projects that use Maven, Gradle, Ivy, or SBT.

## Manifest Files
FossID-DA can analyze the following Java/Scala/Kotlin manifest files:
- Maven: `pom.xml`
- Gradle: `build.gradle`, `build.gradle.kts`, `gradle.properties`, `libs.versions.toml`
- Ivy: `ivy.xml`, `build.xml`
- SBT: `build.sbt`
- Kotlin: `build.gradle.kts`, `libs.versions.toml`

## Key Configuration Options

### Environment Settings
- `da_maven_version`: Maven version to use for dependency resolution
- `da_scala_version`: Scala version to use for resolution

### Processing Options
- `da_allow_dynamic_scopes`: Process custom-defined dependency scopes

### Dependency Scopes
- `da_ds_plugin_dependencies`: Process Maven plugins that extend build functionality
- `da_ds_extensions_dependencies`: Process Maven extensions
- `da_ds_provided_dependencies`: Process dependencies provided by the runtime environment
- `da_ds_runtime_dependencies`: Process dependencies required at runtime
- `da_ds_library_dependencies`: Process library dependencies
- `da_ds_framework`: Process framework dependencies (often for Scala)
- `da_ds_classpath_dependencies`: Process classpath dependencies
- `da_ds_test_dependencies`: Process "test" scope in Maven
- `da_ds_optional_dependencies`: Process optional dependencies in Maven

### Dependency Tree Depth
- `da_gd_maven`: Maximum depth for the dependency tree traversal

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 