# Privacy Policy: Time Tracker - Offline

**Effective date: 2026-11-07**

Time Tracker - Offline is an offline time-tracking application published by
nawki for the Microsoft Store.

## Data collection

The app does not collect, store, transmit, or share any user data with the
developer or any third party. Specifically:

- The app makes **no network requests of its own**. It has no server, and none
  of your time entries, categories, notes, activity or settings ever leave your
  device. The only traffic is Windows asking the Microsoft Store about Pro, as
  described under In-app purchases.
- The app includes **no telemetry, analytics, or crash reporting**.
- The app includes **no auto-update logic**; updates are delivered exclusively
  by the Microsoft Store.
- The app does not require **any user account or sign-in**.
- The app does not use your **microphone, camera or location**, and it refuses
  every such permission. Its spellchecker is off, so it downloads no
  dictionaries.

## In-app purchases

Time Tracker Pro is an optional Yearly subscription or Lifetime purchase.
Either plan unlocks the same Pro features, including all export formats.

Windows checks Pro licenses and completes purchases through
Windows.Services.Store in the bundled StoreHelper. Time entries, activity
records and other app content are never included in these requests. Microsoft
handles its own account, purchase and subscription information.

While the app is running, Windows asks the Microsoft Store whether you own Pro:

- when the app starts, when the PC wakes from sleep and when you choose Check
  purchases;
- on the renewal date of a Yearly plan;
- every 15 minutes while a purchase you just made is not yet in your license;
- every 30 minutes during the week after a Yearly plan's renewal date, until
  the renewal is confirmed.

Prices are requested only when you open Plan or the unlock dialog, or start a
purchase, and are kept in memory for the session.

Manage subscription opens https://account.microsoft.com/services in your browser
only when you click it. It does not send app content to that page.

Leave a review (the star in the sidebar, Settings > About, or the occasional
prompt after a saved timer session) opens the Microsoft Store's review page
for Time Tracker, only when you click it. Time Tracker sends nothing; what you
write there goes to Microsoft under its own terms. Whether to show the prompt
is decided on your device from how many entries you have and how old the
first one is; at most two prompts, months apart, and none after you open the
review page.

If you unlock Pro with a license key instead, the key is verified entirely on
your device using cryptography built into the app. No network request is made
on that path at all. A copy of the key is kept at
`Documents\Time Tracker\license.json` so it survives resetting or reinstalling
the app. That file holds the key, a random identifier for this install and the
date the app was first used. It contains no time-tracking data. Deleting it is
safe.

## Data storage

Everything you create is stored on your device, in the app's data folder:

`%APPDATA%\time-tracker`

In the Microsoft Store version, Windows keeps that folder inside the app's own
package storage
(`%LOCALAPPDATA%\Packages\nawki.TimeTracker-Offline_...\LocalCache\Roaming\time-tracker`)
and deletes it when you uninstall or reset the app.

The folder holds:

- `data\timetracker.db`, a SQLite database with your categories, time entries,
  planner, rates, invoices, budgets, report presets, Pro settings and, if you
  turn it on, the activity timeline.
- The app's display and timer settings (theme, Show seconds, day start, daily
  goal and similar), whether and when you were asked for a review, and a
  running timer with its description, in the app's local storage
  (`Local Storage\leveldb`). The database also keeps a copy of
  the day start, daily goal, week start and clock format, which totals,
  budgets, reports and notifications use; the rest is not part of the
  database file and does not travel with it or with backups.
- Copies the app keeps for itself in the `data` folder: one taken before a
  database upgrade (the newest two are kept) and one taken before a restore
  replaces your data (the newest three are kept).
- The working files of Electron, the framework the app is built on, such as
  caches.

These files are visible to other applications running under your Windows user
account and are subject to whatever backup, sync, or access your operating
system provides. It is your data. You can open, inspect, copy, or delete it
at any time.

Exports (CSV, JSON, PDF and Excel) are generated locally and saved to the
location you choose. Nothing is uploaded during export.

## Activity timeline

The activity timeline is optional and off by default. When enabled, it records
the foreground application locally: its executable name and the name the
program gives itself, such as "Google Chrome". Recording window titles is a
separate opt-in. Exclusions are applied before titles are read. No activity is
uploaded or used for telemetry.

You can pause recording, choose how long activity is kept, and delete it.
Delete activity history works on every plan, also after Pro ends. It removes
the activity from the database and from the copies the app keeps for itself
(see Data storage). If one of those copies cannot be changed, for example a
damaged one, it names the file so you can delete it yourself. Turning window
titles off, excluding an app and keeping activity for a shorter time remove
the same way what they no longer allow. Backups you made yourself are your
files and are not changed.

## Backups, invoices and reports

Backups, invoices and scheduled monthly reports are created locally in the
folders you choose. Backups can be encrypted with a passphrase. Time Tracker
does not upload them. A folder managed by another sync or backup service is
subject to that service's behavior. Keep a backup passphrase safe; Time Tracker
cannot recover a forgotten passphrase.

## Contact

For questions about this policy, contact nawki at yusufnawki@gmail.com.

Send feedback (in Settings, the sidebar and the command palette) opens a new
email to that address in your own email app, only when you click it. Time
Tracker fills in only the address and a subject with the app's version, such
as "Time Tracker 1.2.0 feedback". It adds no message text, diagnostics or data
and sends nothing itself; the email goes only if you send it.

## Changes

If this policy changes in a future version, the updated text will be published
at the same URL and the effective date above will be updated.

Version 1.2.0 removed voice quick add, so the app no longer uses the
microphone. This text now also lists each time the Microsoft Store is asked
about Pro, where settings and the app's own copies are kept, what the
feedback email contains, and what Leave a review opens.
