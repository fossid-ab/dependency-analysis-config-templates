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
  Affects POM resolution strategy and repository access
- `da_scala_version`: Scala version to use for resolution
  Impacts cross-version dependencies and Scala library resolution

### Processing Options
- `da_allow_dynamic_scopes`: Process custom-defined dependency scopes
  Important for Maven/Gradle projects with custom scope definitions

### Dependency Scopes
- `da_ds_plugin_dependencies`: Process Maven build plugins (<build><plugins>) that may contain dependencies
- `da_ds_extensions_dependencies`: Process Maven build extensions that alter build behavior (<build><extensions>)
- `da_ds_provided_dependencies`: Process dependencies marked as <scope>provided</scope> (e.g., servlet-api, javax)
- `da_ds_runtime_dependencies`: Process dependencies marked as <scope>runtime</scope> or default compile scope
- `da_ds_library_dependencies`: Process SBT/Scala libraryDependencies
- `da_ds_framework`: Process Framework dependencies in SBT/Scala projects
- `da_ds_classpath_dependencies`: Process Dependencies added directly to classpath rather than declared in POM
- `da_ds_test_dependencies`: Process Dependencies marked as <scope>test</scope> (JUnit, TestNG, Mockito)
- `da_ds_optional_dependencies`: Process Dependencies marked with <optional>true</optional>

### Dependency Tree Depth
- `da_gd_maven`: Maximum depth for the dependency tree traversal (5 is the default)

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 