# office-cli Distribution

This repository publishes public release assets for the closed-source `office-cli` binary.

## Install

### macOS (Homebrew)

```bash
brew tap officecli/office-cli
brew install officecli/office-cli/office-cli
```

To update later:

```bash
brew upgrade officecli/office-cli/office-cli
```

### Linux

```bash
curl -fsSL https://raw.githubusercontent.com/officecli/office-cli-dist/main/scripts/install-office-cli.sh | DIST_REPO=officecli/office-cli-dist bash
```

Re-running the same installer command refreshes the local binary to the latest published version.

If your shell still reports `office-cli: command not found`, first try:

```bash
export PATH="$HOME/.local/bin:$PATH"
office-cli --version
```

If that works, add `~/.local/bin` to your shell startup file so future shells can find the command.

To install a specific version, set `VERSION` before invoking the script:

```bash
curl -fsSL https://raw.githubusercontent.com/officecli/office-cli-dist/main/scripts/install-office-cli.sh | VERSION=v0.1.1 DIST_REPO=officecli/office-cli-dist bash
```

## Manual Download

Download archives and `checksums.txt` from the Releases page of this repository.

## Notes

- This repository contains binaries, checksums, and install helpers only.
- It does not contain `office-cli` source code.
