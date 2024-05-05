# Versions.json

[<- Back](README.md)

This json document should contain a listing of every file inside the Universal Application Package package, along with a [semver](https://semver.org/) version of that file. The json schema should be as below

```json
{
  "Binaries": {
    "linux": {
      "x64/application": "1.0.0",
      "x64/library.so": "1.0.0",
      "rv64/application": "1.0.0",
      "rv64/library.so": "1.0.0",
      "arm64/application": "1.0.0",
      "arm64/library.so": "1.0.0"
    },
    "windows": {
      "x64/application.exe": "1.0.0",
      "x64/library.dll": "1.0.0",
      "x86/application.exe": "1.0.0",
      "x86/library.dll": "1.0.0",
      "rv64/application.exe": "1.0.0",
      "rv64/library.dll": "1.0.0",
      "arm64/application.exe": "1.0.0",
      "arm64/library.dll": "1.0.0"
    }
  },
  "ApplicationData": {
    "locals/en-us.dat": "1.0.3",
    "locals/pt-br.dat": "1.0.2",
    "startup.ogg": "1.0.5"
  },
  "Logos": {
    "logo.svg": "1.0.1",
    "x3.png": "1.0.2"
  }
}
```

At the root of the document, the "Binaries", "ApplicationData" and "Logos" represents every folder inside the Universal Application Package, items inside each folder should contain paths relative to each folder's parent object

## Example

```json
{
  "Logos": {
    "logo.svg": "1.0.0"
  }
}
```

The `logo.svg` file inside `Logos` folder gets represented as a `Logos` object with another object inside of it for the `logo.svg` file along with it's version
