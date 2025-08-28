# 🚀 Custom Wake-On-LAN TUI 🚀

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Made with Bash](https://img.shields.io/badge/Made%20with-Bash-1f425f.svg)](https://www.gnu.org/software/bash/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
[![GitHub issues](https://img.shields.io/github/issues/LINUX-OASIS/NETWORKING-WAKE-ON-LAN)](https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN/issues)
[![GitHub forks](https://img.shields.io/github/forks/LINUX-OASIS/NETWORKING-WAKE-ON-LAN)](https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN/network)
[![GitHub stars](https://img.shields.io/github/stars/LINUX-OASIS/NETWORKING-WAKE-ON-LAN)](https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN/stargazers)

A powerful, TUI-based (Text User Interface) shell script for managing and sending Wake-On-LAN (WOL) magic packets to devices on your network. Built with `bash` and `whiptail` for a user-friendly experience right in your terminal.

!demo
>_(Note: GIF is for illustrative purposes)_

---

## ✨ Features

*   **Interactive TUI Menu:** Easy navigation and operation powered by `whiptail`.
*   **Network Scanning:** Discovers potential WOL targets on a selected network interface using `netdiscover`.
*   **Target Management:** Save, delete, and manage a persistent list of WOL targets.
*   **🏷️ Nicknames:** Assign custom nicknames to your saved devices for easy identification.
*   **🚀 Dual-Method Wake-Up:** Uses both `etherwake` and `wakeonlan` to maximize compatibility and success rate.
*   **📦 Automatic Dependency Installation:** Checks for required packages and attempts to install them automatically.
*   **🛡️ Root/Sudo Enforcement:** Automatically prompts for and re-runs with `sudo` if not run as root.

---

## 🖥️ Compatibility

This script is designed for Debian-based Linux distributions that use the `apt` package manager. It is known to be compatible with:

*   Debian
*   Ubuntu (and flavors like Kubuntu, Xubuntu)
*   Linux Mint
*   ...and other Debian derivatives.

---

## ⚙️ Dependencies

The script relies on a few command-line tools to function correctly. It will automatically check if they are installed and attempt to install them for you using `sudo apt install`.

*   `whiptail` (usually pre-installed or available in the `newt-tui` package)
*   `ethtool`
*   `etherwake`
*   `netdiscover`
*   `wakeonlan`

---

## 🛠️ Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN.git
    cd NETWORKING-WAKE-ON-LAN
    ```

2.  **Make the script executable:**
    ```bash
    chmod +x custom-NETWORKING-WAKE-ON-LAN
    ```

3.  **Run the script with root privileges:**
    The script requires root access for network scanning and sending WOL packets. It will attempt to re-launch itself with `sudo` if needed.
    ```bash
    sudo ./custom-NETWORKING-WAKE-ON-LAN
    ```

---

## 🗄️ Configuration

Saved WOL targets are stored in a plain text file located at:
`/bin/CUSTOM-WAKE-ON-LAN-TARGETS/WAKE-ON-LAN-TARGETS.txt`

Each line in the file represents a target in the format:
`<INTERFACE> <MAC_ADDRESS> <IP_ADDRESS> :: <NICKNAME>`

> **Note:** Storing configuration data in `/bin` is non-standard. This may be changed in future versions to a more appropriate location like `/etc/` or a user's home directory to better follow the Filesystem Hierarchy Standard (FHS).

---

## 💬 Contributing

[Pull requests, issues, and suggestions are warmly welcomed!](https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN/issues)

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 🌐 Links

*   [Issues](https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN/issues)
*   [Pull Requests](https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN/pulls)
*   [Releases](https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN/releases)
*   [Wiki](https://github.com/LINUX-OASIS/NETWORKING-WAKE-ON-LAN/wiki)

---

## 🧙‍♂️ Maintainer

*   [LINUX-OASIS](https://github.com/LINUX-OASIS)

---

## 📜 License

This project is licensed under the **GPL-3.0 License**. See the [LICENSE](LICENSE) file for details.
