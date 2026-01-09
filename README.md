# wujihand-hmi

  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Release](https://img.shields.io/github/v/release/wuji-technology/wujihand-hmi)](https://github.com/wuji-technology/wujihand-hmi/releases)

  Wuji Hand HMI is a cross-platform graphical user interface application for Wuji Hand dexterous hand control and monitoring. It provides real-time device status and sensor data display, built-in calibration and debugging tools, and robust batch operation handling. Supports both Windows and Linux platforms with improved Ubuntu compatibility.

  - **Status Monitoring**: Real-time display of device status and sensor data with optimized log display
  - **Calibration Functions**: Built-in device calibration and debugging tools
  - **Batch Operations**: Robust exception handling for batch operations
  - **Cross-platform**: Support for Windows and Linux platforms with improved Ubuntu compatibility

  ## Table of Contents

  - [Usage](#usage)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Running](#running)
  - [Troubleshooting](#troubleshooting)
  - [Appendix](#appendix)
  - [Contact](#contact)

  ## Usage

  ### Prerequisites

  **Windows**
  - Windows 11 (64-bit)
  - 200MB available disk space

  **Linux**
  - Ubuntu 22.04 LTS / Ubuntu 24.04 LTS (x86_64)
  - 200MB available disk space

  ### Installation

  **Windows**

  Download and run the installer:

  ```bash
  wujihand-qt-hmi_v1.1.0.exe
  ```

  **Linux**

  Extract and run:

  ```bash
  # Extract the package
  tar -xzvf wujihand-qt-hmi_v1.1.0-linux.tar.gz

  # Navigate to the extracted directory
  cd wujihand-qt-hmi_v1.1.0/

  # Run the application
  ./wujihand-qt-hmi_v1.1.0
  ```

  ### Running

  #### 1. Launch Application

  ```bash
  # Windows
  wujihand-qt-hmi_v1.1.0.exe

  # Linux
  cd wujihand-qt-hmi_v1.1.0/
  ./wujihand-qt-hmi_v1.1.0
  ```

  #### 2. HMI Usage Tutorial

  **Documentation Link**: [Wuji Hand Usage Tutorial](https://docs.wuji.tech/)

  #### Configuration

  **Communication Configuration**

  Connect Wuji Hand dexterous hand via USB

  #### Project Structure

  **Windows Version**

  ```text
  wujihand-qt-hmi_v1.1.0/
  ├── wujihand-qt-hmi_v1.1.0.exe     # Main program
  ├── bin/                           # wujihub runtime library files
  ├── config/                        # Configuration files
  ├── _internal/                     # Internal dependency library files
  ```

  **Linux Version**

  ```text
  wujihand-qt-hmi_v1.1.0/
  ├── wujihand-qt-hmi_v1.1.0.bin     # Main program
  ├── bin/                           # wujihub
  ├── config/                        # Configuration files
  ```

  ## Troubleshooting

  1. **Application won't start**

     Check error logs for detailed information. Keep logs and contact customer support.

  2. **Device connection failed**

     - Check if device is properly connected
     - Verify port configuration is correct
     - Check firewall settings
     - Check permission settings

  3. **UI display issues**

     - Update graphics drivers
     - Check system DPI settings
     - Try running as administrator
     - Adjust screen scaling to 100%

  ## Appendix

  - **Project Homepage**: [https://github.com/wuji-technology/wujihand-hmi](https://github.com/wuji-technology/wujihand-hmi)
  - **Issue Tracker**: [https://github.com/wuji-technology/wujihand-hmi/issues](https://github.com/wuji-technology/wujihand-hmi/issues)
  - **Documentation**: [Wuji Hand Usage Tutorial](https://docs.wuji.tech/)

  > **Note**: This project is under active development and features may change. Please check for updates regularly.

  ## Contact

  For any questions, please contact support@wuji.tech.
