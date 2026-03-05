# wujihand-hmi

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Release](https://img.shields.io/github/v/release/wuji-technology/wujihand-hmi?display_name=tag)](https://github.com/wuji-technology/wujihand-hmi/releases)

Wuji Hand HMI is a cross-platform graphical user interface application for Wuji Hand dexterous hand. It provides real-time device status monitoring, built-in calibration and debugging tools, and supports both Windows and Ubuntu.

**Get started with [Quick Start](#quick-start). For detailed documentation, please refer to [HMI User Guide](https://docs.wuji.tech/docs/en/wuji-hand/latest/wuji-hand-hmi-user-guide/) on Wuji Docs Center.**

## Quick Start

### Installation

Download the latest package from [GitHub Releases](https://github.com/wuji-technology/wujihand-hmi/releases/latest).

**Windows**

Extract the package, then double-click `wuji-hand-hmi_<version>-windows` to launch.

**Ubuntu**

```bash
sudo apt install ./wuji-hand-hmi_<version>_amd64.deb
```

Open from the application menu, or run `wuji-hand-hmi` in the terminal.

### Connect and enable

1. Connect Wuji Hand via USB, select the correct port, and click **Connect**.
2. Click **Enable** to power all joint motors.
3. Click **Run Demo** to verify communication and motion.

## Troubleshooting

1. **Port access permission (Ubuntu)**

   If you can't find the port when launching the Ubuntu HMI:
   - Method 1: Add the current user to the `dialout` group
     ```bash
     sudo usermod -a -G dialout $USER
     ```
     After execution, apply the permissions:
     - Current terminal only: `newgrp dialout`
     - System-wide: `sudo reboot`

   - Method 2: Launch the HMI with sudo
     ```bash
     sudo wuji-hand-hmi
     ```

2. **Display scaling warning**

   If a display scaling warning appears during startup, adjust the display scaling to 100% (1:1) in your system settings, then restart the HMI.

## Contact

For any questions, please contact [support@wuji.tech](mailto:support@wuji.tech).
