---
title: System76 Software (Install - Other Operating Systems)
description: >
  Learn what software is needed to use other OSes and install them
keywords:
  - system76
  - support

facebookImage: /_social/article
twitterImage: /_social/article

hidden: false
section: software
tableOfContents: true
---

## Disclaimer

Except in some rare cases, System76 QA and Engineering teams do not test other OSes on our hardware. This section is provided for informational purposes only. System76 encourages users to take ownership of their machines and install whatever software or operating systems they prefer.

However, System76 does not guarantee the success or quality of experience when installing other Operating Systems.
Support typically makes best-efforts to offer direction or troubleshooting for other distributions.

We may determine that troubleshooting has exceeded the scope of support. If that's the case, further questions should be referred to those Operating System(s)' support forums.

**NOTE:** These instructions were tested on a Galago Pro (galp3-b) and Pangolin (pang10). Neither system have NVIDIA GPUs, so this process doesn't go over installing the NVIDIA driver (system76-driver-nvidia). Due to these limitations, switchable graphics may not work on NVIDIA systems.

## Arch

Be sure to install the <u>System76 Driver</u> first. The steps to do that are [here](/articles/system76-driver).

If you want to use an AUR helper like [Paru](https://github.com/Morganamilo/paru) then follow the steps on this [page](/articles/system76-driver) as well.

This command will install all of the packages using <u>Paru</u>.

```bash
paru -S system76-firmware-daemon system76-firmware firmware-manager system76-power gnome-shell-extension-system76-power-git system76-driver system76-dkms system76-acpi-dkms
```

This command will install `firmware-manager` using <u>Paru</u>.

**NOTE:** choose the first software option after running the <u>Paru</u> command.

```bash
paru -s firmware-manager
```

### System76 DKMS

This package is needed for hotkeys and fan(s) on Closed Firmware systems.

```bash
git clone https://aur.archlinux.org/system76-dkms.git
cd system76-dkms
makepkg -srcif
```

This command will install `system76-dkms` using <u>Paru</u>.

**NOTE:** choose the first software option after running the <u>Paru</u> command.

```bash
paru -s system76-dkms
```

### System76 ACPI DKMS

This package is needed for hotkeys and fan(s) on Open Firmware systems.

```bash
git clone https://aur.archlinux.org/system76-acpi-dkms.git
cd system76-acpi-dkms
makepkg -srcif
```

This command will install `system76-acpi-dkms` using <u>Paru</u>.

**NOTE:** choose the first software option after running the <u>Paru</u> command.

```bash
paru -s system76-acpi-dkms
```

### System76 Power

```bash
git clone https://aur.archlinux.org/system76-power.git
cd system76-power
makepkg -srcif
sudo systemctl enable --now com.system76.PowerDaemon.service
sudo gpasswd -a $USER adm
```

These commands will install `system76-power` using <u>Paru</u>.

**NOTE:** choose the first software option after running the <u>Paru</u> command.

```bash
paru -s system76-power
sudo systemctl enable --now com.system76.PowerDaemon.service
sudo gpasswd -a $USER adm
```

### System76 Power GNOME Shell Extension

```bash
git clone https://aur.archlinux.org/gnome-shell-extension-system76-power-git.git
cd gnome-shell-extension-system76-power
makepkg -srcif
```

This command will install `gnome-shell-extension-system76-power` using <u>Paru</u>.

**NOTE:** choose the first software option after running the <u>Paru</u> command.

```bash
paru -s gnome-shell-extension-system76-power
```

### System76 Thelio Io DKMS

```bash
git clone https://aur.archlinux.org/system76-io-dkms.git
cd system76-io-dkms
makepkg -srcif
```

This command will install `system76-io-dkms` using <u>Paru</u>.

**NOTE:** choose the first software option after running the <u>Paru</u> command.

```bash
paru -s system76-io-dkms
```

**NOTE:** This package is only needed for Thelio desktops.

### System76 OLED

```bash
git clone https://aur.archlinux.org/system76-oled.git
cd system76-acpi-oled
makepkg -srcif
```

This command will install it using <u>Paru</u>.

**NOTE:** choose the first software option after running the <u>Paru</u> command.

```bash
<u>Paru</u> -s system76-acpi-oled
```

**NOTE:** This package is only needed for systems with OLED displays to control the brightness.

## Fedora

Be sure to install the <u>System76 Driver</u> first. The steps to do that are [here](/articles/system76-driver).

### System76 Firmware Manager in Fedora

Then install the <u>System76 Firmware Manager</u> and the <u>System76 Firmware Daemon</u>, enable the service and add your user to the adm group.

```bash
sudo dnf install firmware-manager
sudo systemctl enable --now system76-firmware-daemon
sudo gpasswd -a $USER adm
```

### System76 Power in Fedora

Use these commands to install the <u>System76 Power</u> package and enable the service:

```bash
sudo systemctl enable system76-power system76-power-wake
sudo systemctl start system76-power
```

### System76 Power GNOME Shell Extension in Fedora

These commands will download the source code for the application, build it, install it and install the <u>Extensions</u> application:

```bash
git clone https://github.com/pop-os/gnome-shell-extension-system76-power.git
cd gnome-shell-extension-system76-power
sudo dnf install nodejs-typescript
make
make install
```

Now log out and use the <u>Extensions</u> to enable the extenstion.

### System76 DKMS in Fedora

These commands will be used to install the <u>System76 DKMS</u> package which is for Proprietary Firmware systems:

```bash
sudo dnf install system76-dkms
sudo systemctl enable dkms
```

### System76 ACPI DKMS in Fedora

These commands will be used to install the <u>System76 ACPI DKMS</u> package which is for Open Firmware systems:

```bash
sudo dnf install system76-acpi-dkms
sudo systemctl enable dkms
```

**NOTE:** After enabling the dkms systemd service for either the <u>System76 DKMS</u> or the <u>System76 ACPI DKMS</u> package you will need to reboot the system:

```bash
sudo systemctl reboot
```

### System76 Thelio Io DKMS in Fedora

This command will be used to install the <u>System76 Io DKMS</u> which is used for the Thelio Io board:

```bash
sudo dnf install system76-io-dkms
```

### System76 OLED in Fedora

This command will be used to install the <u>System76 OLED</u> which is used for systems with OLED panels:

```bash
sudo dnf install system76-oled
```
