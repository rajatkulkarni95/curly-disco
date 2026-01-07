---
title: "Storing Data"
source: "https://docs.octarine.app/core-concepts/storing-data"
description: "How Octarine interacts and stores data for settings and notes"
published: "2026-01-07"
clipped_at: "2026-01-07T10:39:52.835Z"
---

# Storing Data

![](https://docs.octarine.app/api/og?title=Storing+Data&description=How+Octarine+interacts+and+stores+data+for+settings+and+notes)

Octarine stores your notes as Markdown-formatted plain text files in a workspace. A workspace is a folder on your file system.

Octarine continously *watches* your workspace folder for an external changes, and makes instant reflection of it in the app. Given that you are working with folder and plain text files, these can be edited by any external text editor of your choosing.

A workspace folder can be created anywhere on your device, including in cloud drives like iCloud, Dropbox local folders.

This is never synced with any service (GitSync, iCloud) or never reaches any servers. This is kept completely on device for security purposes.

Please ensure you don’t make any changes or delete this without creating a backup, since deletion could have irreversible changes.

You can refresh a database by using `Cmd/Ctrl + K → Refresh Database` to force the database to re-index everything.

Note: Ask Octarine and Writing Assistant history as well as Recently Viewed will be wiped clean and can’t be recovered when this is done. Be careful.