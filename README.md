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
- **Automated nightly builds**: every push to develop or master resets a rolling [nightly pre-release](../../releases/tag/nightly), and each platform uploads its own installers, portable builds and checksums as soon as it finishes building, no waiting for the whole matrix.
- **Automated daily sync with upstream**: upstream develop is merged automatically and pushed; on conflict the merge is aborted and a tracking issue is opened for a human or an AI agent to fix.
- **Release builds only**: CI never produces Debug artifacts and never compiles tests.
- **Three build targets**: Linux x64, Windows MSVC x64 and macOS arm64 (Apple Silicon). MinGW-w64, Windows arm64 and Linux arm64 builds are dropped.
- **x86-64-v3** on Linux and Windows, so those builds need an AVX2-era CPU (roughly 2013 or newer); macOS ships arm64.
- **Compiler optimization and binary size flags**: whole program optimization and LTO, aggressive inlining, fast floating point, control flow guard, dead code elimination, hidden symbol visibility and stripped release binaries.
- **Newest stable Qt**, currently **6.11.2**, pinned once for all platforms.
- **Runner images**: Ubuntu 24.04, Windows Server 2022 with Visual Studio 2022 and macOS 26, with every GitHub Action pinned to an exact commit sha.
- **CI caching** for compiler output (sccache), vcpkg dependencies and Qt downloads.
- Trimmed this README down to the essentials.

## Installation

This fork is built from develop, so there are no stable releases. Download the latest build from the rolling [nightly pre-release](../../releases/tag/nightly), or grab per-commit artifacts from the [GitHub Actions](../../actions) tab.

## License [![License](https://img.shields.io/github/license/Mitra-88/PrismLauncher?label=License&logo=gnu&color=C4282D)](LICENSE)

All launcher code is available under the GPL-3.0-only license.

The logo and related assets are under the CC BY-SA 4.0 license.
