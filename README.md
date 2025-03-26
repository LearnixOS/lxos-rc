<div align="center">


<img src="https://raw.githubusercontent.com/LearnixOS/learnixos.github.io/refs/heads/main/assets/images/logo.png" align="center" alt=" Preview" width="250" style="display: block; margin: 32px auto; border: 2px solid #555; border-radius: 12px; box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);">

<div align="center">

# lxos-rc: Simple Init for LearnixOS

## Dependencies
### Core Requirements
- **BusyBox** (or equivalent): Provides `sh`, `mount`, `umount`, `sync`, `poweroff`, `pidof`, etc.
- **iproute2**: For `ip` command in `rc.network`.

### Service-Specific Dependencies
- **alsa-utils**: For `rc.alsa` (`alsactl`).
- **bluez**: For `rc.bluetooth` (`bluetoothd`).
- **wpa_supplicant**: For `rc.wpa_supplicant` (Wi-Fi).
- **dhcpcd**: For IP assignment in `rc.network` and `rc.wpa_supplicant`.
- **e2fsprogs**: For `rc.fsck` (`fsck`).
- **busybox-syslogd** (or standalone `syslogd`): For `rc.syslog`.

### Optional
- **hwclock**: For clock setup in `/etc/lxos-rc` (via `rc.conf`).
- A kernel with `procfs`, `sysfs`, `devtmpfs`, and hardware module support (e.g., `bluetooth`).

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/LearnixOS/lxos-rc.git
   cd lxos-rc
