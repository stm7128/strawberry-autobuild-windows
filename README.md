# strawberry-autobuild-windows

---

[![Build](https://github.com/stm7128/strawberry-autobuild-windows/actions/workflows/build.yml/badge.svg)](https://github.com/stm7128/strawberry-autobuild-windows/actions/workflows/build.yml)

**English** | [日本語](https://github.com/stm7128/strawberry-autobuild-windows/blob/main/README.jp.md)

This repository provides unofficial **Windows builds** of [Strawberry Music Player](https://github.com/strawberrymusicplayer/strawberry).

**Downloads:** You can download the latest unofficial builds from the [**Releases page**](https://github.com/stm7128/strawberry-autobuild-windows/releases/latest).

Official builds for Windows are not currently available directly from the main project for all users. However, [instructions for building from source](https://github.com/strawberrymusicplayer/strawberry#wrench-compiling-from-source) can be found in the official repository.


## Available Builds

This repository provides the following types of Windows builds. Builds are automatically generated daily (and on pushes to the `main` branch of this repository) from the latest code of the official Strawberry repository.

| Toolchain | Architecture | Build Type | Notes |
| :--- | :--- | :--- | :--- |
| **MSVC (Microsoft Visual C++)** | `x86_64` (64-bit) | Release, Debug | **Recommended for most users** |
| | `x86` (32-bit) | Release, Debug | |
| | ~~`arm64`~~ | ~~Release~~, ~~Debug~~ | **Discontinued due to being unstable and unverifiable.** |
| **MinGW (MinGW-w64 GCC)** | `x86_64` (64-bit) | Release, Debug | Alternative build using GCC |
| | `x86` (32-bit) | Release, Debug | |

- **Release:** Optimized builds for everyday use. Most users should choose this.
- **Debug:** Larger builds intended for developers or for troubleshooting specific issues.



## Important Note

*   **Updater Disabled:** The built-in updater in these unofficial builds is intentionally disabled. This is because this build is provided independently, and using the official updater mechanism could cause confusion or direct users of this unofficial build to the official Patreon page, which is intended for supporters of the official project. To update, please download the latest version from the [Releases page](https://github.com/stm7128/strawberry-autobuild-windows/releases/latest) of this repository.

## Issues and Support

*   For any bugs, issues, or feature requests related to **Strawberry's functionality**, please submit them on the official [Strawberry Issues page](https://github.com/strawberrymusicplayer/strawberry/issues). The developers at Strawberry may be able to assist with issues via GitHub.
    *   *Examples: Music playback stutters, a specific file format doesn't work, a feature request for a new audio output.*

*   If you encounter issues specifically with the **build process, the installers, or the availability of builds provided by *this* repository**, please [open an issue here](https://github.com/stm7128/strawberry-autobuild-windows/issues).
    *   *Examples: The installer fails to run, a downloaded file is corrupt, a scheduled build has failed.*

This repository does not offer official support for Strawberry Music Player itself.

## License

Strawberry Music Player is licensed under the GPLv3. These unofficial builds are also provided under the terms of the GPLv3.

## Support Official Development

Thank you for using this unofficial build of Strawberry Music Player. If you enjoy the software, please consider supporting the official development of Strawberry Music Player through the following options. Supporting the **official developer directly** helps ensure the continued development and maintenance of Strawberry.

- [Patreon](https://www.patreon.com/jonaskvinge) - Supporters often receive access to official builds; check their page for current benefits and tiers.
- [GitHub Sponsors](https://github.com/sponsors/jonaski)
- [Ko-fi](https://ko-fi.com/jonaskvinge) - Official builds may also be available to supporters here; please see their page for details.
- [PayPal](https://paypal.me/jonaskvinge)
