# strawberry-autobuild-windows

This repository provides unofficial **Windows builds** of [Strawberry Music Player](https://github.com/strawberrymusicplayer/strawberry).

**Downloads:** You can download the latest unofficial builds from the [**Releases page**](https://github.com/stm7128/strawberry-autobuild-windows/releases).

Official builds for Windows are not currently available directly from the main project for all users. However, [instructions for building from source](https://github.com/strawberrymusicplayer/strawberry#wrench-compiling-from-source) can be found in the official repository.

## Available Builds

This repository provides the following types of Windows builds. Builds are automatically generated daily (and on pushes to the `main` branch of this repository) from the latest code of the official Strawberry repository.

*   **MSVC (Microsoft Visual C++) Builds:**
    *   Architectures: `x86` (32-bit), `x86_64` (64-bit), `arm64`
    *   Build Types: Release, Debug
    *   These are generally recommended for most users on Windows.

*   **MinGW (MinGW-w64 GCC) Builds:**
    *   Architectures: `i686` (32-bit), `x86_64` (64-bit)
    *   Build Types: Release, Debug
    *   Provides an alternative build using the GCC toolchain.

**Note:** ARM64 builds are currently only available for the MSVC version.

## Important Notes

*   **Updater Disabled:** The built-in updater in these unofficial builds is intentionally disabled. This is because this build is provided independently, and using the official updater mechanism could cause confusion or direct users of this unofficial build to the official Patreon page, which is intended for supporters of the official project. To update, please download the latest version from the [Releases page](https://github.com/stm7128/strawberry-autobuild-windows/releases) of this repository.

## Issues and Support

*   For any bugs, issues, or feature requests related to **Strawberry's functionality**, please submit them on the official [Strawberry Issues page](https://github.com/strawberrymusicplayer/strawberry/issues). The developers at Strawberry may be able to assist with issues via GitHub.
*   If you encounter issues specifically with the **build process, the installers, or the availability of builds provided by *this* repository**, please [open an issue here](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY/issues).

This repository does not offer official support for Strawberry Music Player itself.

## License

Strawberry Music Player is licensed under the GPLv3. These unofficial builds are also provided under the terms of the GPLv3.

## Support Official Development

Thank you for using this unofficial build of Strawberry Music Player. If you enjoy the software, please consider supporting the official development of Strawberry Music Player through the following options:

- [Patreon](https://www.patreon.com/jonaskvinge)
- [GitHub Sponsors](https://github.com/sponsors/jonaski)
- [Ko-fi](https://ko-fi.com/jonaskvinge)
- [PayPal](https://paypal.me/jonaskvinge)

Your support helps ensure the continued development and maintenance of Strawberry.
