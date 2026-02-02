# wujihand-hmi

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Release](https://img.shields.io/github/v/release/wuji-technology/wujihand-hmi)](https://github.com/wuji-technology/wujihand-hmi/releases)

wujihand-hmi is a comprehensive Python SDK for controlling and communicating with Wuji Hand dexterous robotic hands. It provides stable device communication interfaces, a graphical user interface with real-time data visualization, and ROS bridge support. The SDK features a modular architecture with separate driver, application, and configuration layers for flexible development.

## Table of Contents

- [Repository Structure](#repository-structure)
- [Usage](#usage)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running](#running)
- [Build & Package](#build--package)
- [Configuration](#configuration)
- [Testing](#testing)
- [Contact](#contact)

## Repository Structure

```text
wujihand-hmi/
├── src/
│   ├── wujihand_py/           # Main package source code
│   │   ├── app/               # GUI application layer
│   │   ├── driver/            # Device drivers
│   │   ├── scripts/           # Utility scripts
│   │   └── config/            # SDK default configuration
│   └── user_test/             # User test code
│       ├── scripts/           # Test scripts
│       └── config/            # User configuration
├── bin/                       # Binary files
├── ci_scripts/                # CI/CD scripts
├── docker_build/              # Docker build files
├── docs/                      # Documentation
└── hooks/                     # Git hooks
```

### Directory Description

| Directory | Description |
|-----------|-------------|
| `src/` | Main source code directory |
| `src/wujihand_py/` | Core SDK package with driver and GUI components |
| `src/user_test/` | User test scripts and configuration |
| `bin/` | Binary executable files |
| `ci_scripts/` | Continuous integration scripts |
| `docker_build/` | Docker build configuration |
| `docs/` | Project documentation |
| `hooks/` | Git hook scripts |

## Usage

### Prerequisites

- Python >= 3.10
- PySide6 (Qt6)
- Ubuntu 22.04 LTS / Ubuntu 24.04 LTS (x86_64) or Windows 11 (64-bit)

### Installation

```bash
# Clone the repository
git clone https://github.com/wuji-technology/wujihand-hmi.git
cd wujihand-hmi

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate  # Linux
# or .venv\Scripts\activate  # Windows

# Install dependencies
pip install -r requirements.txt
```

### Running

```bash
# Activate virtual environment
source .venv/bin/activate

# Run GUI application (main entry)
PYTHONPATH=src python src/user_test/scripts/qt_test.py

# Run standalone GUI (no device required)
PYTHONPATH=src python src/user_test/scripts/qt_test_standalone.py

# Run SDO communication test
PYTHONPATH=src python src/user_test/scripts/sdo_test.py

# Run PDO communication test
PYTHONPATH=src python src/user_test/scripts/pdo_test.py

# Check device info
PYTHONPATH=src python src/user_test/scripts/check_info.py
```

## Build & Package

### Build for Ubuntu

```bash
# Activate virtual environment
source .venv/bin/activate

# Build with wujihub (recommended)
./reset_params_install.sh wujihand_qt_hmi_Ubuntu_with_wujihub.spec

# Build without wujihub
./reset_params_install.sh wujihand_qt_hmi_Ubuntu.spec
```

### Build for Windows

```bash
pyinstaller wujihand_qt_hmi_Windows.spec
```

Build output will be in `dist/` directory:
- `wujihand-qt-hmi`: Main executable
- `bin/wujihub`: WujiHub daemon (if using `_with_wujihub.spec`)
- `config/`: Configuration files

## Configuration

### Basic Configuration

Configure basic parameters in `src/wujihand_py/config/user_param.yaml`:

```yaml
device:
  local_host: 192.168.128.2
  remote_host: 192.168.128.1
```

### User Configuration

Configure user-specific parameters in `src/user_test/config/user_params.yaml`:

```yaml
device:
  local_host: 192.168.128.2
  remote_host: 192.168.128.1
```

## Testing

Test scripts are located in `src/user_test/scripts/`:

| Script | Description |
|--------|-------------|
| `qt_test.py` | GUI functionality test |
| `qt_test_standalone.py` | Standalone GUI test (no device) |
| `pdo_test.py` | PDO communication test |
| `sdo_test.py` | SDO communication test |
| `check_info.py` | Device information query |

## Contact

For any questions, please contact support@wuji.tech.
