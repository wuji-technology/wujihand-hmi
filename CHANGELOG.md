# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Added doc mode sanitizer (`WUJIHAND_DOC_MODE` env var) to replace sensitive info (version, SN, IP, URL, date) with placeholders in UI for documentation screenshots

### Fixed
- Fixed GitHub Actions workflow error: removed invalid `secrets` context reference from `if` condition
- Fixed Windows build artifact uploading PyInstaller intermediate files (`base_library.zip`) instead of final zip only

## [1.5.1] - 2026-02-02

### Fixed
- Fixed slider jumping issue when SLIPPED error occurs with firmware v1.2.1

## [1.5.0] - 2026-01-19

### Fixed

- Fixed demo_record_angles to mirror left_angles to right_angles
- Set iq_limit to 1500 for running routines
- Fixed permission issues for config and log files in Ubuntu (recursive nested directory permissions)
- Adjusted top panel UI component sizes to optimize layout
- Fixed device connection guide and help documentation links

### Changed

- Renamed "IQ Limit" to "Effort Limit"
- Changed unit from mA to A (default 1.5A, range 0-3.5A)
- Updated tooltip with Effort definition description

## [1.4.0] - 2025-12-31

### Added

- Demo mode supports loop playback and speed adjustment
- Added Docker build support for Ubuntu 22.04
- Added RPDO/TPDO diagnostic control functionality

### Changed

- Product renamed to Wuji Hand HMI

## [1.3.0] - 2025-12-19

### Added

- Added device serial number (SN) read/write functionality
- Added single instance detection to prevent multiple program instances
- Added motor error status monitoring and alerts
- Added system version and joint information display
- Added automatic log cleanup functionality

### Changed

- Prioritized display of electrical angle and cogging torque information

### Fixed

- Fixed startup crash on Linux systems
- Fixed demo mode auto-switch issue
- Fixed multi-language adaptation for help documentation links

## [1.1.0] - 2025-10-16

### Added

- Added splash screen
- Added automatic version check and update notification
- Added log file size limit and automatic rotation
- Added position error threshold highlighting
- Added FCL control mode support

### Changed

- Optimized logging system performance

### Fixed

- Fixed trajectory playback stability issues
- Fixed calibration status UI display issues
- Fixed factory reset dialog layout

[Unreleased]: https://github.com/wuji-technology/wujihand-hmi/compare/v1.5.1...HEAD
[1.5.1]: https://github.com/wuji-technology/wujihand-hmi/compare/v1.5.0...v1.5.1
[1.5.0]: https://github.com/wuji-technology/wujihand-hmi/compare/v1.4.0...v1.5.0
[1.4.0]: https://github.com/wuji-technology/wujihand-hmi/compare/v1.3.0...v1.4.0
[1.3.0]: https://github.com/wuji-technology/wujihand-hmi/compare/v1.1.0...v1.3.0
[1.1.0]: https://github.com/wuji-technology/wujihand-hmi/compare/v1.0.0...v1.1.0
