# Metadata.json

[< Back](README.md)

This json document should contain metadata about the application inside the Universal Application Package, The json schema should be as below:

```json
{
  "id": "application.developer",
  "developer": {
    "name": "Visible name in UI's",
    "email": "contact.email@developer.com",
    "website": "Application Website / Github"
  },
  "platforms": {
    "linux": {
      "minkernel": "6.8.7",
      "executables": {
        "x86-64": "linux_x86-64/application",
        "rv64": "linux_rv64/application",
        "arm64": "linux_arm64/application"
      }
    },
    "windows": {
      "minbuild": "19045.4355",
      "minversion": "10.0.18362.592",
      "executable": {
        "x86-64": "windows_x86-64/application",
        "x86": "windows_x86/application",
        "arm64": "windows_arm64/application"
      }
    }
  },
  "logo": {
    "svg": "logo.svg",
    "2x": "logo_x2.png"
  }
}
```
