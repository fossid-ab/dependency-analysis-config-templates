# Dart/Flutter Configuration for FossID-DA

This directory contains a sample configuration file for Dart and Flutter projects that use Pub.

## Manifest Files
FossID-DA can analyze the following Dart manifest files:
- Pub: `pubspec.yaml`, `pubspec.lock`

## Key Configuration Options

### Processing Options
- `da_ignore_lock_manifests`: Ignore lock files (pubspec.lock) and use pubspec.yaml

### Dependency Scopes
- `da_ds_dependency_overrides`: Process "dependency_overrides" section in pubspec.yaml

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 