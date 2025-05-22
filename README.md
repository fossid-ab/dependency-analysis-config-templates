# FossID-DA Sample Configuration Files

This repository contains ready-to-use [Settings Files](https://eval-eu.foss.id/cs-demo/help/en/fda/FossID-DA-Settings-File.html) for FossID Dependency Analysis (FDA) that include all available settings that apply to each programming language ecosystem it can analyze. 

Each configuration file is organized into logical sections:

- `[dependency-analysis]`: Enables the package managers to analyze.
- `[dependency-analysis.system_settings]`: Language/package manager versions and OS settings
- `[dependency-analysis.scan_options]`: Controls how FDA processes manifests and source files
- `[dependency-analysis.dependency_scopes]`: Controls which dependency scopes are analyzed
- `[dependency-analysis.graph_depth]`: Controls how deep dependency trees are traversed
- `[dependency-analysis.ignore_settings]`: Controls which folders to ignore during analysis

For any settings not defined in the settings file, FDA will read from the Global Settings defined in the FossID Configuration (fossid.conf). These settings files focus only on language-specific settings that may vary by project.

## Supported Language Ecosystems
Each language directory contains a sample `fossid-settings.toml` file that can be copied to your project's root directory to tell FDA how you want it to analyze your project.

| Language/Ecosystem | Directory | Supported Package Managers |
|-------------------|-----------|----------------------------|
| JavaScript/Node.js | [javascript/](javascript/) | NPM, Yarn, PNPM, Bower |
| Java/Scala/Kotlin | [java/](java/) | Maven, Gradle, Ivy, SBT |
| Python | [python/](python/) | PIP, Pipenv, Poetry, Hatch |
| Ruby | [ruby/](ruby/) | Bundler, Gem |
| .NET/C# | [dotnet/](dotnet/) | NuGet |
| Go | [go/](go/) | Go Modules, Dep, Glide, Godep |
| C/C++ | [cpp/](cpp/) | Conan, CMake |
| PHP | [php/](php/) | Composer |
| Swift/Objective-C | [swift/](swift/) | CocoaPods, Carthage, Swift Package Manager |
| Rust | [rust/](rust/) | Cargo |
| Dart/Flutter | [dart/](dart/) | Pub |
| Haskell | [haskell/](haskell/) | Cabal, Stack |
| Elixir | [elixir/](elixir/) | Hex, Mix |
| Bazel | [bazel/](bazel/) | Bazel build system |
| Pants | [pants/](pants/) | Pants build system |
| Yocto | [yocto/](yocto/) | Yocto, BitBake |
| Android Soong | [soong/](soong/) | Android build system |

## How to Use these Configuration Files

1. Choose the configuration file for your project's programming language
2. Copy the `fossid-settings.toml` file from the corresponding directory to your project's root directory
3. Customize the settings as needed for your specific project requirements

## What if my Project uses multiple languages?
Simply put the contents from multiple configuration files into a single one! 