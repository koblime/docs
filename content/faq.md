---
title: FAQ
label: FAQ
icon: question
order: 50
---

# Frequently Asked Questions

## What makes up Koblime

Koblime is made up of the following components:

* API Server
* Web App
* Kobo App

## What is installed on my device

The KoboRoot.tgz file consists of the following:

* config.yaml
* koblime
* udev
* nm

## Google Drive picker won't open

You may see *"We can't access this content right now. Try signing into your Google
account or allowing cookie access to proceed."*

When you click **Add Book** (or **Link**) in the web app, Koblime opens Google's
file picker so you can choose an `.epub` from your Google Drive. The picker runs
inside a window served by Google, and to show your files it needs to read your
**Google sign-in cookie**. Some browsers block this by default because the picker
is loaded from a different site (`google.com`) than Koblime — which causes the
messages above.

To fix it:

1. **Make sure you're signed into Google in the same browser.** Open a new tab,
   go to [accounts.google.com](https://accounts.google.com), and sign in with the
   Google account that holds your books.
2. **Allow third-party cookies for kobli.me** using the steps for your browser
   below.
3. Reload the Koblime page and try **Add Book** again. Cookie changes can take a
   moment to take effect.

### Chrome / Edge

Chrome and Edge usually work without changes. If the picker is blocked:

* Click the **eye / tracking icon** at the right-hand side of the address bar.
* Choose **Allow third-party cookies** for this site.

Or go to `Settings → Privacy and security → Third-party cookies`, choose
**"Sites allowed to use third-party cookies"**, click **Add**, and enter
`[*.]kobli.me`. This only affects Koblime.

### Firefox

* Click the **shield icon** in the address bar.
* Turn **Enhanced Tracking Protection** to **Off** for this site.

This change applies only to Koblime; protection stays on everywhere else.

### Safari

Safari does not offer a per-site setting, so the option is global:

* Open `Safari → Settings → Privacy`.
* Uncheck **"Prevent cross-site tracking."**
* Make sure you are signed in at [accounts.google.com](https://accounts.google.com).

You can turn **"Prevent cross-site tracking"** back on after you have linked your
books — it only needs to be off while you use the picker.

> Once a book is linked, syncing and downloading it to your Kobo does **not**
> require these cookie settings. They are only needed while choosing files in the
> Google Drive picker.