# Helium Scoop Bucket

A [Scoop](https://scoop.sh/) bucket for installing the [Helium Browser](https://github.com/imputnet/helium-windows) on Windows.

**Note**: This project is not affiliated with Helium Browser or Imputnet. Report installation bugs to this repository.

## Available Packages

### Installer-based

- `helium` - Latest stable release
- `helium-nightly` - Latest nightly build

### Portable (no installer required)

- `helium-portable` - Latest stable release (portable zip)
- `helium-nightly-portable` - Latest nightly build (portable zip)

## Installation

### Add the bucket

```powershell
scoop bucket add helium https://github.com/Jasdeep-Dhillon/helium-scoop
```

### Install a package

| Version                 | Command                                        |
| ----------------------- | ---------------------------------------------- |
| helium                  | `scoop install helium/helium`                 |
| helium-nightly          | `scoop install helium/helium-nightly`          |
| helium-portable         | `scoop install helium/helium-portable`         |
| helium-nightly-portable | `scoop install helium/helium-nightly-portable` |

## Auto-Update

All package manifests include `checkver` and `autoupdate` configuration, allowing Scoop to automatically detect new upstream releases and update package URLs and hashes.

## Project Structure

```
helium-scoop/
  bucket/
    helium.json                  # Stable installer manifest
    helium-portable.json         # Stable portable manifest
    helium-nightly.json          # Nightly installer manifest
    helium-nightly-portable.json # Nightly portable manifest
  bin/
    checkver.ps1        # Version checking script
    checkhashes.ps1     # Hash verification
    checkurls.ps1       # URL verification
    auto-pr.ps1         # Auto PR creation for updates
    formatjson.ps1      # JSON formatting
    test.ps1            # Manifest testing
```

## Credits

- [Helium-Chromium](https://github.com/imputnet/helium-chromium)
- [Helium-Windows](https://github.com/imputnet/helium-windows)
- Grayscale icon adapted from [Helium Icon](https://github.com/imputnet/helium-chromium/blob/main/resources/branding/app_icon/raw.png)

## License

MIT
