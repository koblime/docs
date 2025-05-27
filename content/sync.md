---
title: Sync
icon: sync
order: 500
---

Koblime performs a wirelesses sync of your Kobo database to https://kobli.me each time your device connects to WiFi.

## What is synced

Koblime sync currently syncs side loaded book `content` and `Bookmarks` table in the `KoboReader.sqlite` database on your device.

When a book is removed from a device, Kobo deletes all reading history, highlights and annotations. You can re-add the book but this information is gone. Koblime prevents the new blank information from overwriting the synced progress.

Sync only copies over book progress if the `TimeSpentReading` of the book on the device is greater than what is already on the server. This way, if you re-add a book to the blank.

> At this time, Koblime does not restore progress or alter the Kobo database in any way. We are looking for beta testers to ensure that we can safely restore sync progress across devices.

## Manual Sync

To manually sync Koblime from your Kobo, you will need Telnet or SSH access to the device. Once you have terminal access to the device, run the following to sync your kobo:

```bash
/opt/bin/koblime
```

The output from this command can help diagnose sync errors.

## Manual Sync from a Computer

We will be releasing a Koblime Command Line App that will allow you to sync your Kobo database using a Computer like so:

```bash
koblime --src <path to KoboReader.sqlite> --token <token> --device <deviceID>
```

This would be an option if you would prefer not to have WiFi sync from the device.
