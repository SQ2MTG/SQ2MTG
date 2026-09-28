# INSTALINUX — Debian/Ubuntu deployment helper

## Purpose

INSTALINUX is a Bash/whiptail interactive script for automating initial configuration of fresh Debian and Ubuntu systems. The current README identifies version `0.6` and the `0.6` branch as the documented release line.

## Requirements

* Debian or Ubuntu;
* root or sudo-capable user;
* Bash, whiptail and apt.

The script can install missing interactive dependencies such as whiptail/dialog and sudo at startup.

## Workflow

The main workflow performs privilege escalation, checks available disk space, presents interactive package selections, optionally installs additional software and performs cleanup.

The README documents a warning when disk usage exceeds **85%**, with the user able to continue or abort.

## Base package options

The interactive package catalogue includes Git, OpenSSH client, curl, wget, gzip, make, CMake, build-essential, gdebi, htop, rdate, Node.js/npm, PHP and audio packages based on ALSA utilities/development libraries.

## Optional software

Documented optional installers include:

* `/etc/rc.local` compatibility;
* RTL-SDR drivers and kernel blacklist configuration;
* RSP1/libmirisdr support;
* WireGuard;
* ZeroTier;
* Cockpit;
* Docker, Docker Compose and Portainer agent;
* Lynis security auditing.

The script also creates working directories under `/opt/log`, `/opt/skrypty`, `/opt/backup` and `/opt/cloud`.

## Tested systems

The README lists Debian 11, 12 and 13 plus Ubuntu 22.04 and 24.04 as tested systems.

## Security considerations

INSTALINUX is a privileged system-modification script. It can install packages, alter sudo configuration, modify kernel module blacklists, install VPN/container software and create directories under `/opt`. Review the exact script revision before execution and run it only on systems where these changes are intended.

## License

The repository README declares the project as MIT licensed.

## Source

Repository: SQ2MTG/instalinux
