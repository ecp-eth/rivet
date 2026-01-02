# Rivet

Rivet is a Foundry version manager that ensures the correct Foundry version is installed and used based on a `.foundry-version` file in your project root.

**Homebrew installed foundry is not supported**: Foundry installed via homebrew does not support version pinning, please uninstall it before using rivet.

## What it does:

- Version detection: Searches for a `.foundry-version` file in the current directory and parent directories
- Installation: Installs Foundry if it's not present
- Version management: Updates Foundry to the target version if there's a mismatch
- Command proxy: Acts as a wrapper for Foundry commands (forge, cast, anvil, chisel)

## Usage

Install Rivet as dev dependency in your project, then prefix the foundry commands with `rivet`:

```json
{
  "scripts": {
    "build": "rivet forge build --sizes --skip test"
  }
}
```
