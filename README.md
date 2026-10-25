# Realme GT6 (RMX3800) Droidspaces-Enabled Boot Image

Custom/Tuned Kernel boot image extracted directly from realme GT6 (RMX3800, Realme UI 16 / Android 16, build `RMX3800_16.0.3.510(CN01)`) with full Linux container / namespace support enabled for **Droidspaces** & Docker.

## Kernel Info
- **Kernel Release**: `6.1.118-Gold_bug`
- **Build**: `#1 SMP PREEMPT aarch64`
- **Compatibility**: Realme GT6 (RMX3800 / Snapdragon 8s Gen 3 / SM8635) running Android 15 / Android 16
- **Tested with**: Droidspaces v7.0.0 (High-performance Container Runtime for Android/Linux)

## Droidspaces Requirement Audit
```
[MUST HAVE]
  [✓] Root privileges
  [✓] Linux version (6.1.118)
  [✓] PID namespace
  [✓] Mount namespace
  [✓] UTS namespace
  [✓] IPC namespace
  [✓] pivot_root syscall
  [✓] /proc filesystem
  [✓] /sys filesystem
  [✓] Seccomp support

[RECOMMENDED & OPTIONAL]
  [✓] epoll support, signalfd, PTY, devpts
  [✓] Loop device & ext4 filesystem
  [✓] Cgroup v2 & Cgroup namespace
  [✓] FUSE & TUN/TAP support
  [✓] OverlayFS support
  [✓] Network namespace & Bridge device support
  [✓] Veth pair support
  [✓] Sandboxing (user namespaces)
```

## Flashing Instructions
Boot your phone into Fastboot mode, then flash into the boot partition:
```bash
# Direct fastboot flash:
fastboot flash boot boot_rmx3800_droidspaces_goldbug.img
fastboot reboot
```

## Downloads
Grab the full 192MB boot image from the [GitHub Releases](https://github.com/Haoduo9/RMX3800-Droidspaces-Kernel/releases) section.
- **File**: `boot_rmx3800_droidspaces_goldbug.img`
- **Size**: 201,326,592 bytes (192MB)
- **MD5**: `85682132103cbcd1b2b633066ae7b31d`
