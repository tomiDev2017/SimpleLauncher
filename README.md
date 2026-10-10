
<div align="center">

# SimpleLauncher

**A lightweight Minecraft launcher for managing and launching Minecraft installations.**

A Windows Minecraft launcher built with Python, CustomTkinter, and minecraft-launcher-lib.

![Windows](https://img.shields.io/badge/platform-Windows-0078D4?style=flat-square&logo=windows)
![Python](https://img.shields.io/badge/python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![CustomTkinter](https://img.shields.io/badge/built_with-CustomTkinter-1F6FEB?style=flat-square)
![Minecraft](https://img.shields.io/badge/Minecraft-Launcher-62B47A?style=flat-square)

</div>

---

# Overview

SimpleLauncher is a lightweight Minecraft launcher designed to make managing different Minecraft installations simple.

It provides a graphical interface where you can create installations, select Minecraft versions, choose custom game directories, and launch Minecraft.

The launcher is built with Python and uses minecraft-launcher-lib to install and launch Minecraft versions.

---

# Features

- 🎮 Launch Minecraft directly from the launcher
- 📦 Install Minecraft versions automatically
- 🗂️ Create multiple installations
- ✏️ Edit existing installations
- 🗑️ Delete custom installations
- 📁 Choose custom game directories
- 🔎 Browse for folders with Windows File Explorer
- 🏠 Home page
- ⚙️ Installation manager
- 💾 Automatically save installation profiles
- 🆕 Latest Version profile
- 🕐 Oldest Version profile
- 🖥️ Windows .exe support
- 🌙 Dark interface
- 🚫 No Microsoft login system

---

# Installation

## Requirements

- Windows
- Python 3.10 or newer
- Internet connection when installing Minecraft versions

## Clone the repository

    git clone https://github.com/tomiDev2017/SimpleLauncher.git
    cd SimpleLauncher

## Install dependencies

    pip install minecraft-launcher-lib customtkinter

## Run SimpleLauncher

    python SimpleLauncher.py

---

# Building the EXE

SimpleLauncher can be compiled into a standalone Windows executable using PyInstaller.

## Install PyInstaller

    pip install pyinstaller

## Build

    pyinstaller --onefile --windowed --name "SimpleLauncher" SimpleLauncher.py

The finished executable will be located at:

    dist\SimpleLauncher.exe

You can then run SimpleLauncher.exe without opening Python manually.

---

# Installations

SimpleLauncher uses installation profiles to keep different Minecraft versions and directories organized.

Each installation contains:

| Setting | Description |
|---|---|
| Name | The name shown in the launcher |
| Minecraft Version | The Minecraft version to launch |
| Game Directory | Where the Minecraft files are stored |

## Example

    PvP
    Minecraft 1.8.9
    C:\Minecraft\PvP

    Latest
    Minecraft 1.21.x
    C:\Minecraft\Latest

    Modded
    Minecraft 1.20.1
    C:\Minecraft\Modded

---

# Default Installations

SimpleLauncher automatically creates two default installations.

## Latest Version

Uses the latest Minecraft release available through minecraft-launcher-lib.

## Oldest Version

Uses the oldest release version returned by minecraft-launcher-lib.

These default installations cannot be deleted.

---

# Custom Game Directories

Each installation can have its own Minecraft directory.

For example:

    C:\Minecraft\1.8.9
    C:\Minecraft\1.12.2
    C:\Minecraft\1.20.1

This makes it possible to keep different installations separated.

You can select a directory using the Browse button in the installation editor.

---

# How Launching Works

When you press Play, SimpleLauncher:

1. Checks the selected Minecraft version.
2. Creates the game directory if necessary.
3. Installs the required Minecraft files.
4. Creates the Minecraft launch command.
5. Starts Minecraft.

Minecraft installation and launching are handled through minecraft-launcher-lib.

---

# Project Structure

    SimpleLauncher/
    ├── SimpleLauncher.py
    ├── requirements.txt
    ├── README.md
    └── .gitignore

The profiles.json file is generated automatically when the launcher is used.

---

# Dependencies

SimpleLauncher uses:

| Library | Purpose |
|---|---|
| customtkinter | Graphical user interface |
| minecraft-launcher-lib | Minecraft installation and launching |
| pyinstaller | Building the Windows executable |

Install the runtime dependencies with:

    pip install -r requirements.txt

---

# requirements.txt

Your requirements.txt should contain:

    minecraft-launcher-lib
    customtkinter

---

# Configuration

Installation profiles are stored locally in:

    profiles.json

The launcher automatically creates and updates this file.

## Example

    [
        {
            "name": "Latest Version",
            "version": "1.x.x",
            "directory": "C:\\Users\\User\\.minecraft"
        }
    ]

You normally do not need to edit this file manually.

---

# Development

Clone the repository:

    git clone https://github.com/tomiDev2017/SimpleLauncher.git
    cd SimpleLauncher

Install dependencies:

    pip install -r requirements.txt

Run the launcher:

    python SimpleLauncher.py

After making changes, rebuild the executable:

    pyinstaller --onefile --windowed --name "SimpleLauncher" SimpleLauncher.py

---

# Contributing

Contributions are welcome!

If you find a bug or have an idea for a feature, you can:

- Open an issue
- Suggest a feature
- Submit a pull request
- Improve the documentation

Please keep contributions related to SimpleLauncher.

---

# Disclaimer

SimpleLauncher is an independent project and is **not affiliated with, endorsed by, or sponsored by Mojang Studios or Microsoft**.

Minecraft and related trademarks belong to their respective owners.

This project does not distribute Minecraft game files.

Users are responsible for having the appropriate Minecraft access and complying with the applicable Minecraft/Mojang/Microsoft terms.

---

# License

This project does not currently include a license.

If you decide to open-source the project, add a LICENSE file to specify how others may use, modify, and distribute the code.

---

# Built With

<div align="center">

**Python** · **CustomTkinter** · **minecraft-launcher-lib** · **PyInstaller**

</div>
