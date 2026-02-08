# strawberry-autobuild-windows

---

[![Build](https://github.com/stm7128/strawberry-autobuild-windows/actions/workflows/build.yml/badge.svg)](https://github.com/stm7128/strawberry-autobuild-windows/actions/workflows/build.yml)

**English** | [日本語](https://github.com/stm7128/strawberry-autobuild-windows/blob/main/README.jp.md)

This repository provides unofficial **Windows builds** of [Strawberry Music Player](https://github.com/strawberrymusicplayer/strawberry).

**Downloads:** You can download the latest unofficial builds from the [**Releases page**](https://github.com/stm7128/strawberry-autobuild-windows/releases/latest).

Official builds for Windows are not currently available directly from the main project for all users. However, [instructions for building from source](https://github.com/strawberrymusicplayer/strawberry#wrench-build-from-source) can be found in the official repository.

## Available Builds

Builds are automatically generated daily (and on pushes to the `main` branch) from the latest code of the official Strawberry repository.

| Toolchain | Architecture | Build Type | Notes |
| :--- | :--- | :--- | :--- |
| **MSVC (Microsoft Visual C++)** | `x64` (64-bit) | Release, Debug | **Recommended** for most Windows users. |
| | `x86` (32-bit) | Release, Debug | For older 32-bit Windows systems. |
| | `arm64` | Release, Debug | **Experimental** (Untested). |
| **MinGW (MinGW-w64 GCC)** | `x64` (64-bit) | Release, Debug | Alternative build using the GCC toolchain. |
| | `x86` (32-bit) | Release, Debug | |

- **Release:** Optimized for performance and everyday use.
- **Debug:** Includes symbols for troubleshooting. Larger file size, intended for developers.

## Important Notes

- **Updater Disabled:** The built-in auto-updater is intentionally disabled. This is to avoid confusion with official release channels and to ensure that users of this unofficial build do not inadvertently bypass the official project's support mechanisms. To update, please download the latest version manually from this repository.
- **ARM64 Experimental Status:** ARM64 builds are provided on an experimental basis. As the maintainer does not own a physical ARM64 Windows device (e.g., Snapdragon X Elite/Plus), **these builds are entirely untested**. If you are using an ARM64 device, we would greatly appreciate your feedback (success or failure) via [GitHub Issues](https://github.com/stm7128/strawberry-autobuild-windows/issues).

## Transparency

To ensure security and reliability, all builds are automated via [GitHub Actions](https://github.com/stm7128/strawberry-autobuild-windows/actions). 
The following modifications are made during the build process:
- The auto-updater is disabled via CMake configuration (`-DENABLE_QTSPARKLE=OFF`).
- The NSIS installer script (`.nsi`) is patched to match this configuration.
- No other modifications are made to the original Strawberry source code.

## Issues and Support

- **For Strawberry functionality bugs:** (e.g., playback issues, UI bugs, feature requests), please report them to the [official Strawberry Issues page](https://github.com/strawberrymusicplayer/strawberry/issues).
  - *Note: Please mention that you are using an **unofficial build** when reporting issues to the official project.*
- **For build/installer issues:** (e.g., the installer fails to run, missing DLL errors, download links broken), please [open an issue here](https://github.com/stm7128/strawberry-autobuild-windows/issues).

## License

Strawberry Music Player is licensed under the GPLv3. These unofficial builds and the build scripts in this repository are also provided under the terms of the GPLv3.

## Support Official Development

If you enjoy Strawberry Music Player, please consider supporting the official developer, **Jonas Kvinge**. Direct support helps maintain the project and ensures its future development.

- [Patreon](https://www.patreon.com/jonaskvinge) - Supporters often receive access to official builds; check their page for current benefits and tiers.
- [GitHub Sponsors](https://github.com/sponsors/jonaski)
- [Ko-fi](https://ko-fi.com/jonaskvinge) - Official builds may also be available to supporters here; please see their page for details.
- [PayPal](https://paypal.me/jonaskvinge)