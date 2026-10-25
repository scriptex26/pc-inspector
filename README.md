# PC Pocket Inspector

A lightweight Windows PC hardware-report tool.

PC Pocket Inspector collects information about your computer's hardware and system and lets you save reports as text or JSON.

**Project status:** Early prototype. Some hardware details may be unavailable or inaccurate depending on Windows, drivers and hardware.

## Features

- System and Windows information
- Processor model, cores and reported clock speeds
- Installed and available RAM
- Graphics adapters and driver versions
- Motherboard and BIOS information
- Drive capacity and free space
- Network adapter information
- Export reports as TXT or JSON
- Copy reports to the clipboard

## For users: Run the app

**Recommended: Download `PC Pocket Inspector.exe` from the GitHub Releases page.**

1. Download the executable from the latest release.
2. Save it somewhere convenient on your Windows PC.
3. Double-click `PC Pocket Inspector.exe`.
4. Click **Generate hardware report**.

You do not need Python or PyInstaller installed to run the standalone executable. The `.exe` is all you need for normal use.

Only run software you trust. Windows may warn about unsigned executables.

## For developers: Run from source

Use this option to inspect, modify and test the code.

**Requirements:** Python 3. No third-party packages are required to run the source.

1. Clone or download this repository.
2. Open Command Prompt in the project folder.
3. Run:

```bat
py pc_pocket_inspector.py
```

Detailed Windows hardware information is collected using PowerShell and Windows system-management information.

## For developers: Build the Windows executable

Build on a Windows computer.

Install PyInstaller:

```bat
py -m pip install --upgrade pyinstaller
```

Build the executable:

```bat
py -m PyInstaller --clean --onefile --windowed --name "PC Pocket Inspector" pc_pocket_inspector.py
```

The executable will be created at:

`dist\PC Pocket Inspector.exe`

Test the executable on another compatible Windows PC before publishing it.

## Privacy

Reports may contain your computer name, IP addresses, MAC addresses, hardware models and driver details. **Review reports before sharing them publicly.**

PC Pocket Inspector is designed for read-only reporting. It does not intentionally change system settings or delete files.

## Contributing

Bug reports, suggestions and code contributions are welcome.

When reporting a problem, include your Windows version, app version, expected behaviour, actual behaviour and any relevant error messages. Remove personal information from reports before attaching them to public issues.

## Licence

This project is intended to use the MIT License. Add a `LICENSE` file with the standard MIT licence text before publishing the project.
