# Swift/Objective-C Configuration for FossID-DA

This directory contains a sample configuration file for Swift and Objective-C projects that use CocoaPods, Carthage, or Swift Package Manager.

## Manifest Files
FossID-DA can analyze the following Swift/Objective-C manifest files:
- CocoaPods: `Podfile`, `Podfile.lock`
- Carthage: `Cartfile`, `Cartfile.resolved`, `Cartfile.lock`
- Swift Package Manager: `Package.swift`

## Key Configuration Options

### Environment Settings
- `da_os_type`: Operating system type (important for Swift/Objective-C dependencies)
- `da_cocoapod_version`: CocoaPods version to use for resolution
- `da_swift_version`: Swift version to use for resolution
- `da_git_user`: GitHub username for API requests
- `da_git_token`: GitHub token for API requests (highly recommended to avoid rate limits)

### Processing Options
- `da_ignore_lock_manifests`: Ignore lock files (Podfile.lock, Cartfile.resolved) and use manifests

### Dependency Tree Depth
- `da_gd_cocoapod`: Maximum depth for the dependency tree traversal

## Usage
Copy `fossid-settings.toml` to your project's root directory or to the directory specified in your FossID configuration. 