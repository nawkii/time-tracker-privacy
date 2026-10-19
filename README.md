# Privacy Policy: Time Tracker - Offline

**Effective date: 2026-10-19**

Time Tracker - Offline is an offline time-tracking application published by
nawki for the Microsoft Store.

## Data collection

The app does not collect, store, transmit, or share any user data with the
developer or any third party. Specifically:

- The app makes **no network requests of its own**. It has no server, and none
  of your time entries, categories, notes or settings ever leave your device.
- The app includes **no telemetry, analytics, or crash reporting**.
- The app includes **no auto-update logic**; updates are delivered exclusively
  by the Microsoft Store.
- The app does not require **any user account or sign-in**.

## In-app purchases

Time Tracker Pro is an optional Yearly subscription or Lifetime purchase.
Either plan unlocks the same Pro features, including all export formats.

Windows checks Pro licenses and completes purchases through Windows.Services.Store
in the bundled StoreHelper. Prices are requested only when you open Plan or the
unlock dialog, or explicitly start a purchase, and cached for the session.
Time entries, activity records and other app content are never included in these
requests. License checks can run at startup and when you request Check purchases.
Microsoft handles its own account, purchase and subscription information.

Manage subscription opens https://account.microsoft.com/services in your browser
only when you click it. It does not send app content to that page.

If you unlock Pro with a license key instead, the key is verified entirely on
your device using cryptography built into the app. No network request is made
on that path at all.

A copy of your unlock is stored at `Documents\Time Tracker\license.json` so it
survives resetting or reinstalling the app. It contains no time-tracking data.
Deleting it is safe.

## Data storage

All data you create (categories, time entries, settings) is stored locally on
your device in a SQLite database file at:

`%APPDATA%\time-tracker\data\timetracker.db`

This file is visible to other applications running under your Windows user
account and is subject to whatever backup, sync, or access your operating
system provides. It is your data. You can open, inspect, copy, or delete it
at any time.

Exports (CSV, JSON, PDF and Excel) are generated locally and saved to the location you
choose. Nothing is uploaded during export.

## Voice quick add

Voice quick add is optional and off by default. When enabled, the microphone is
used only while you explicitly record a phrase, for up to 30 seconds. Recognition
runs on your device with the bundled model. Audio is held in memory for the
request, not saved as an audio file or sent to a server. You review and can edit
the transcript and parsed entry before saving. Cancel stops recording.

## Activity timeline

The activity timeline is optional and off by default. When enabled, it records
the foreground application locally. Recording window titles is a separate opt-in.
Exclusions are applied before titles are read. You can pause, delete activity
history and choose retention. No activity is uploaded or used for telemetry.

## Backups and invoices

Backups and invoices are created locally in the locations you choose. Backups
can be encrypted with a passphrase. Time Tracker does not upload them. A folder
managed by another sync or backup service is subject to that service's behavior.
Keep a backup passphrase safe; Time Tracker cannot recover a forgotten passphrase.

## Contact

For questions about this policy, contact nawki at yusufnawki@gmail.com.

Send feedback (in Settings, the sidebar and the command palette) opens a new
email to that address in your own email app, only when you click it. Time
Tracker adds nothing to it and sends nothing itself; the email goes only if
you send it.

## Changes

If this policy changes in a future version, the updated text will be published
at the same URL and the effective date above will be updated.
