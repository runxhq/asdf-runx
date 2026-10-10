# asdf-runx

[![Install check](https://github.com/runxhq/asdf-runx/actions/workflows/plugin.yml/badge.svg)](https://github.com/runxhq/asdf-runx/actions/workflows/plugin.yml)

Install [Runx](https://runx.ai) from its published, checksummed CLI archives with [asdf](https://asdf-vm.com/).

```sh
asdf plugin add runx https://github.com/runxhq/asdf-runx.git
asdf install runx latest
asdf set -u runx latest
runx --version
```

The plugin lists published `cli-v` releases only after the archives and checksum sidecars for its supported platforms are present. It installs `runx-js-worker` beside `runx` whenever the archive includes it. Historical archives without a worker remain installable. It does not build Runx or maintain a separate version number.

Supported platforms: macOS and Linux on arm64 or x86_64. The plugin requires curl, jq, tar, and either `sha256sum` or `shasum`.
