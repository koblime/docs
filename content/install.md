---
icon: download
order: 200
---

You can install Koblime from your device by going to the [Devices](https://kobli.me/devices) tab and clicking the install button.

> The resulting `KoboRoot.tgz` contains your Koblime credentials and is specific to the device. Please do not share this file with anyone and installing it on an unintended device will results in books getting attributed to the wrong device.

## What is installed

The installation package contains the following items:

### Configuration

The configuration file is located at `/mnt/onboard/.add/koblime/config.yaml` and contains your DeviceID and Koblime token

### Sync Application

The Sync application is located at `/opt/bin/koblime`. This application is run each time your device sync.

### NickelMenu Item

If you happen to have NickleMenu installed, we add a Koblime menu item to initiate a manual sync at `/mnt/onboard/.adds/nm/koblime`.

> NickleMenu itself is not installed. You will have to do this yourself.

### Udev Rule

Koblime uses [Udev](https://opensource.com/article/18/11/udev) to detect a WiFi connection. The Koblime Usev rule is located at `/etc/udev/rules.d/97-koblime.rules`. This Udev rule runs the Sync Application each time WiFi is detected.
