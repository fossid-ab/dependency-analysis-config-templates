# FossID-DA Sample Configuration Files

This repository contains ready-to-use configuration files for FossID Dependency Analysis (FDA) that include all available settings that apply to each programming language ecosystem it can analyze. 

Each configuration file is organized into logical sections:

- `[dependency-analysis.system_settings]`: Language/package manager versions and OS settings
- `[dependency-analysis.scan_options]`: Controls how FDA processes manifests and source files
- `[dependency-analysis.dependency_scopes]`: Controls which dependency scopes are analyzed
- `[dependency-analysis.graph_depth]`: Controls how deep dependency trees are traversed
- `[dependency-analysis.ignore_settings]`: Controls which folders to ignore during analysis

For a full description of these sections and all available configuration options, visit [FossID-DA Settings Files](https://eval-eu.foss.id/cs-demo/help/en/fda/FossID-DA-Settings-File.html) in the Documentation.

For settings not defined in the settings file, FDA reads the Global Settings in the FossID Configuration (fossid.conf). These settings files focus on language-specific settings that may vary by project.

## How to Use these Configuration Files

1. Choose the configuration file for your project's programming language
2. Copy the `fossid-settings.toml` file from the corresponding directory to your project's root directory
3. Customize the settings as needed for your specific project requirements

## What if my Project uses multiple languages?
Simply put the contents from multiple configuration files into a single one! 

## Support
This repository is maintained by the Customer Success Team. We will do our best to keep it updated as FossID-DA is updated, but we may miss things. If you notice discrepancies or issues please open a support ticket in our [Support Portal](https://support.fossid.com/) or open a PR with a fix if you feel generous. :)