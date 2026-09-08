# Candy Tools — Homebrew Tap

The Homebrew home for Candy Tools, our small collection of command-line
utilities. Tap it once and every tool we ship is just a `brew install` away.

## Install

Add the tap, trust it, then install whatever you need:

```sh
brew tap candy-tools/tap
brew trust candy-tools/tap
brew install todo
```

Prefer to install directly? Using the full name trusts that one tool for you,
so there's no separate trust step:

```sh
brew install candy-tools/tap/todo
```

Update to the latest versions anytime with:

```sh
brew update && brew upgrade
```

## Why the trust step?

Since Homebrew 6.0.0, third-party taps like this one aren't trusted by default —
Homebrew won't run any of their code until you say it's okay. Skip it and you'll
just get a warning, and nothing from the tap will install.

`brew trust candy-tools/tap` trusts everything we publish here, now and in the
future. If you'd rather trust one tool at a time, do that instead:

```sh
brew trust --cask candy-tools/tap/todo
```

See what you've trusted with `brew trust`, and undo it anytime with
`brew untrust candy-tools/tap`.

## Tools

| Tool   | Description                                                           |
| ------ | -------------------------------------------------------------------- |
| `todo` | Keyboard-driven terminal TODO manager backed by plain Markdown files |

New tools show up here as we release them.
