# Candy Tools — Homebrew Tap

Homebrew tap for the Candy Tools command-line utilities. Add this tap once and
install any of our tools with `brew`.

## Install

```sh
brew tap candy-tools/tap
brew install <tool>
```

Or without tapping first:

```sh
brew install candy-tools/tap/<tool>
```

Upgrade later with:

```sh
brew update && brew upgrade
```

## Available tools

Tools are published to this tap automatically as they are released.

<!--
| Tool     | Description |
| -------- | ----------- |
| `tool-a` | ...         |
-->

## Notes

- Tools here are distributed as Homebrew **casks** (prebuilt binaries), which
  are **macOS only** — Linux `brew` users are not covered by casks.
- Nothing in this repository is edited by hand: each tool's release pipeline
  (GoReleaser) commits its generated cask into `Casks/`.

## For maintainers — how a tool publishes here

Add a `homebrew_casks:` block to **each tool's own repository** in its
`.goreleaser.yaml` (not to this repo). A ready-to-copy example lives in
[`examples/example-goreleaser.yaml`](examples/example-goreleaser.yaml).

The release workflow needs a GitHub token with **write access to this tap
repo**, exposed as `TAP_GITHUB_TOKEN` — the default `GITHUB_TOKEN` cannot push
to another repository.
