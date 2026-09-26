<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/program_info/org.prismlauncher.PrismLauncher.logo-darkmode.svg">
  <source media="(prefers-color-scheme: light)" srcset="/program_info/org.prismlauncher.PrismLauncher.logo.svg">
  <img alt="Prism Launcher" src="/program_info/org.prismlauncher.PrismLauncher.logo.svg" width="40%">
</picture>
</p>

<p align="center">
  Prism Launcher is a custom launcher for Minecraft that allows you to easily manage multiple installations of Minecraft at once.<br />
</p>

> **Note:** This repository is an unofficial fork of [Prism Launcher](https://github.com/PrismLauncher/PrismLauncher) and is not endorsed by or affiliated with the Prism Launcher project.

## Changes in this fork

- Based on the latest **develop** branch changes, not the stable release.
- Release-only CI builds with extra compiler optimization and binary size flags: no Debug builds, no CI test compilation.
- Linux and Windows builds target **x86-64-v3**, so they need an AVX2-era CPU (roughly 2013 or newer); macOS ships an **arm64** (Apple Silicon) build.
- Windows builds use MSVC only: MinGW-w64, Windows arm64 and Linux arm64 builds are dropped.
- Newest stable Qt, currently **6.11.2**, pinned for all platforms in one place.
- Automated nightly builds: every push to develop or master replaces the rolling nightly pre-release with fresh installers, portable builds and checksums.
- Automated daily sync with upstream develop: clean merges are pushed automatically, conflicts abort the merge and open a tracking issue for a human or an AI agent to fix.
- CI caching for compiler output (sccache), vcpkg dependencies and Qt.
- Trimmed this README down to the essentials.

## Installation

This fork is built from develop, so there are no stable releases. Download the latest build from the rolling [nightly pre-release](../../releases/tag/nightly), or grab per-commit artifacts from the [GitHub Actions](../../actions) tab.

## License [![License](https://img.shields.io/github/license/Mitra-88/PrismLauncher?label=License&logo=gnu&color=C4282D)](LICENSE)

All launcher code is available under the GPL-3.0-only license.

The logo and related assets are under the CC BY-SA 4.0 license.
