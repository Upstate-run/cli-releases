# Upstate CLI releases

Official prebuilt CLI for [Upstate](https://upstate.run), the read-only overview
and deployment verifier for your Kamal apps. Application source is maintained
separately. This repository contains release artifacts and installation guidance.

## Install

```sh
brew install upstate-run/tap/upstate
upstate version
```

Without Homebrew, download the archive matching macOS/Linux and amd64/arm64 from
[Releases](https://github.com/upstate-run/cli-releases/releases). Verify the
archive against the release's `checksums.txt`, extract it, and install `upstate`
on your PATH. No Go compiler or source checkout is needed.

```sh
cd your-kamal-project
upstate connect --dry-run
upstate connect
kamal deploy
upstate receipt --watch
```

Connect shows proposed changes and preserves existing hooks. Credentials are
stored in protected user configuration, not your repository. The separate
observer uses `ghcr.io/upstate-run/upstate-agent:0.1.5`. Neither the CLI's hosted
API nor the observer provides a remote command channel.

Report problems through the issue tracker without tokens, environment values,
customer logs, or other private data.
