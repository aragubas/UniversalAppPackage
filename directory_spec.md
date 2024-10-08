# Directory Structure

[<- Back](README.md)

All Directories listed in here along with it's usage is **not optional and all files inside a Universal Application Package should not be modified at runtime**, and it must follow the specification strictly to avoid issues with implementations

## /Binaries

Contains binaries for every supported operating system and CPU architecture, organized in a `os_architecture` format called System Identifier

Standard System Identifiers:

| Operating System | CPU Architecture | System Identifier |
| ---------------- | ---------------- | ----------------- |
| Linux            | x64              | linux_x64         |
| Linux            | rv64             | linux_rv64        |
| Linux            | arm64            | linux_arm64       |
| Windows          | x64              | windows_x64       |
| Windows          | x86              | windows_x86       |
| Windows          | arm64            | windows_arm64     |

### Example structure for an application that supports Windows and Linux for x86-64

1. `/Binaries/linux_x86-64/app.x86_64`
1. `/Binaries/windows_x86-64/app.exe`

## /Logos

Contains logos for displaying in operating system menus and package icon in file browsers

There are two valid file types for logos:

1. PNG (Portable Network Graphics)
1. SVG (Scalable Vector Graphics)

All logos should have a 1:1 aspect ratio (square). Filenames should follow the format below, and sizes should be named by powers of 16

For PNG files

- `{size}.png`

For SVG files

- `logo.svg`

### Example Sizes

- 1x = 16x16
- 2x = 32x32
- 3x = 48x48
  [...] and so on

### Example structure for application logos

1. `/Logos/logo.svg`
1. `/Logos/x2.png`
1. `/Logos/x3.png`
1. `/Logos/x4.png`

## /ApplicationData

**Static** application resources/data. **When running a binary, the application working path should be set to this folder**

The contents of this folder is completely dependent on the app vendor and there's no defined structure. **Files inside this folder should NOT be modified by the app at runtime, this folder should be read only**
