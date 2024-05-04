# Universal App Package

Universal app package is a new cross-platform app packaging format for Windows and Linux

A universal app package is a folder with a short and readable name of an application, ending with `.application`

## .application Structure

### /Binaries

Contains directories of binaries for every supported operating system and CPU architecture, organized in a os_architecture format called System Identifiers

Valid System Identifiers:

| Operating System | CPU Architecture | System Identifier |
| ---------------- | ---------------- | ----------------- |
| Linux            | x86-64           | linux_x86_64      |
| Linux            | rv64             | linux_rv64        |
| Linux            | arm64            | linux_arm64       |
| Windows          | x86-64           | windows_x86-64    |
| Windows          | x86              | windows_x86       |
| Windows          | arm64            | windows_arm64     |

#### Example structure for an application that supports Windows and Linux for x86-64

1. `/Binaries/linux_x86-64/app.x86_64`
1. `/Binaries/windows_x86-64/app.exe`

### /Logos

Contains logos for displaying in operating system menus/package icon. There are two valid types of logos:

1. PNG
1. SVG

All logos should have a 1:1 aspect ratio (square) and be organized by powers of 16x16
