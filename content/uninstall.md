---
icon: repo-deleted
order: 100
---

You can uninstall Koblime from your device by going to the [Devices](https://kobli.me/devices) tab and checking the `Uninstall on sync` checkbox. This will uninstall Koblime the next time the device attempts to sync.

## Manual Uninstall

To manually uninstall Koblime from your Kobo, you will need Telnet or SSH access to the device. Once you have terminal access to the device, run the following to remove all Koblime components.

```bash
rm -rf /etc/udev/rules.d/97-koblime.rules
rm -rf /mnt/onboard/.adds/nm/koblime
rm -rf /mnt/onboard/.add/koblime
rm -rf /opt/bin/koblime
reboot
```
