# Medan Installer (Windows MSI)

The official Windows installer for the **Medan** ecosystem.  
This project builds the `.msi` package that installs the Medan CLI and supporting tools on Windows.

Medan is a fast, sandboxed package installer designed for apps, tools, and runtimes.  
Learn more at: https://medan-org.github.io

---

## Features

- Installs the Medan CLI (`medan.exe`)
- Adds Medan to the system PATH
- Supports upgrades (planned)
- Optional Start Menu shortcuts (planned)
- Built using WiX Toolset v4 and .NET SDK

---

## Repository Structure

~~~~text
medan-installer/
│
├── src/
│   ├── MedanInstaller.wixproj   # WiX project file
│   ├── Package.wxs              # Installer definition
│   ├── assets/                  # Icons, license, branding
│   └── medan.exe                # Placeholder binary
│
├── installer/                   # Output folder (empty, tracked with .gitkeep)
├── scripts/                     # Build/automation scripts
├── docs/                        # Documentation
│
├── LICENSE                      # MIT License (Medan default)
├── README.md
└── .gitignore
~~~~

---

## Building the Installer

### Requirements

- **.NET SDK 8+**
- **WiX Toolset v4**
- Windows 10 or later

### Build

From the `src/` directory:

~~~~sh
dotnet build
~~~~

The resulting `.msi` will appear in:

~~~~text
src/bin/Debug/
src/bin/Release/
~~~~

---

## Development Notes

- `medan.exe` is currently a placeholder.  
  The real Medan CLI will be copied in during the build pipeline.
- `assets/` contains installer branding (icons, license text, etc).
- `scripts/` will contain automation for versioning and packaging.
- `docs/` will contain installer architecture and design notes.

---

## Roadmap

- Automatic versioning
- Digital signing support
- Uninstall + repair options
- Registry entries for Medan
- Optional UI for installer

---

## License

This project is licensed under the **MIT License**, the default for all Medan projects.  
See the `LICENSE` file for details.
