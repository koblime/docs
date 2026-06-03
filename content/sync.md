---
title: Sync
icon: sync
order: 200
---

Koblime performs a wirelesses sync of your Kobo database to https://kobli.me each time your device connects to WiFi.

## What is synced

Koblime sync currently syncs side loaded book `content` and `Bookmarks` table in the `KoboReader.sqlite` database on your device.

When a book is removed from a device, Kobo deletes all reading history, highlights and annotations. You can re-add the book but this information is gone. Koblime prevents the new blank information from overwriting the synced progress.

Sync only copies over book progress if the `TimeSpentReading` of the book on the device is greater than what is already on the server. This way, if you re-add a book to the blank.

> At this time, Koblime does not restore progress or alter the Kobo database in any way. We are looking for beta testers to ensure that we can safely restore sync progress across devices.

## Adding books from Google Drive

In the web app, **Add Book** and **Link** open the Google Drive picker so you can
choose an `.epub` to link to a device. The picker is served by Google and needs
your browser to allow Google's sign-in cookie. Chrome and Edge generally work out
of the box; Safari and Firefox block this by default.

If the picker shows *"Can't access this content"* or *"sign into your Google
account,"* see [the FAQ](faq.md#google-drive-picker-wont-open) for the per-browser
cookie steps. Once a book is linked, syncing it to your Kobo does not require any
cookie changes.

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