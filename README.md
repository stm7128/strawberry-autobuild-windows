# strawberry-autobuild-windows


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
| | ~~`x86` (32-bit)~~ | - | **Discontinued.** No longer supported by Qt/Strawberry. |
| | `arm64` | Release, Debug | **Experimental** (Untested). |
| **MinGW (MinGW-w64 GCC)** | `x64` (64-bit) | Release, Debug | Alternative build using the GCC toolchain. |
| | `x86` (32-bit) | Release, Debug | **Deprecated.** Removed upstream; functionality not guaranteed. |

- **Release:** Optimized for performance and everyday use.
- **Debug:** Includes symbols for troubleshooting. Larger file size, intended for developers.

## Important Notes


- **Updater Intentionally Disabled:**
  The built-in auto-updater (Sparkle/QtSparkle) is **disabled** in these builds. This is a deliberate choice for the following reasons:
  1. **UX Consistency:** Since these are unofficial automated builds, the official update channel would repeatedly notify users to "update" to the official release (often pointing to Patreon), which creates a confusing and repetitive loop for users who have chosen to use this specific CI version.
  2. **Technical Compatibility:** These builds are not signed with the official project's certificate, meaning the official auto-updater would fail or point to incompatible binaries.
  3. **Reducing Support Burden:** Disabling the updater prevents users from accidentally "updating" to an official version they may not have access to, and prevents the official developer from receiving irrelevant update-related queries from unofficial build users.
  - *To update, please manually download the latest release from this repository.*
- **x86 (32-bit) Support Status:**
  - **MSVC x86:** These builds are no longer provided. Support for 32-bit x86 architecture has been officially dropped by both the Qt framework and the Strawberry Music Player project.
  - **MinGW x86:** While these builds are currently still being generated, the x86 configuration has been removed from the upstream repository. As a result, **full functionality and stability are not guaranteed**. It is highly recommended to migrate to a 64-bit version of Windows if possible.
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