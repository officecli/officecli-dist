# OfficeCLI Distribution

This repository publishes public release assets for the closed-source `officecli` binary.

## Install

### macOS (Homebrew)

```bash
brew tap officecli/officecli
brew install officecli
```

To update later:

```bash
brew upgrade officecli
```

### Linux

```bash
curl -fsSL https://raw.githubusercontent.com/officecli/officecli-dist/main/scripts/install-officecli.sh | DIST_REPO=officecli/officecli-dist bash
```

By default, the installer downloads and installs the rolling `latest` build from this repository.

Re-running the same installer command refreshes the local binary to the newest rolling latest build.

If your shell still reports `officecli: command not found`, first try:

```bash
export PATH="$HOME/.local/bin:$PATH"
officecli --version
```

If that works, add `~/.local/bin` to your shell startup file so future shells can find the command.

To install a specific published release, set `VERSION` before invoking the script:

```bash
curl -fsSL https://raw.githubusercontent.com/officecli/officecli-dist/main/scripts/install-officecli.sh | VERSION=v0.1.1 DIST_REPO=officecli/officecli-dist bash
```

## Manual Download

Download versioned archives and `checksums.txt` from the Releases page of this repository.

## Notes

- This repository contains binaries, checksums, and install helpers only.
- It does not contain `officecli` source code.
