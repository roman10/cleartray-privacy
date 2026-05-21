# Cleartray Privacy Policy

**Effective date:** 2026-05-21
**App:** Cleartray (Android `app.cleartray`)
**Publisher contact:** feipeng@clarifisg.com

Cleartray is an independent productivity app inspired by the Getting Things Done® (GTD) methodology. This policy explains exactly what the app does — and does not do — with your data.

The short version: **everything you put into Cleartray lives on your device.** The app has no user account, no server backend, and no analytics. Crash reporting is **opt-in and off by default**.

---

## 1. Data you create in the app

Everything you capture in Cleartray — items, projects, contexts, areas, attachments (photos, voice memos), reviews, settings — is written to a local SQLite database in the app's private storage on your device.

We do not transmit this content anywhere. There is no cloud sync, no remote backup, no "Cleartray account." We cannot see your tasks, your notes, or any attachments.

If you uninstall the app, this data is removed by the operating system along with the app's storage. There is no copy held by us to delete on request, because no copy ever leaves your device.

## 2. Backup and restore

Cleartray includes a **JSON export/import** in Settings → Backup. When you tap Export, the app writes a JSON file and hands it to the system share sheet. From there *you* choose where it goes (Files, Drive, email, another app). The file is your data, in plain JSON, under your control. We never receive it.

Restoring works the same way in reverse: you pick a previously exported file and the app reads it locally.

## 3. Permissions and why we ask for them

Cleartray requests these Android permissions. Each is used only for the feature named, and the resulting data stays on your device.

| Permission | What it enables | Data leaves device? |
|---|---|---|
| `POST_NOTIFICATIONS` | Show reminder notifications (due dates, weekly review nudge). | No |
| `USE_EXACT_ALARM` / `SCHEDULE_EXACT_ALARM` | Fire reminders at the exact scheduled minute (inexact alarms drift up to an hour). | No |
| `RECEIVE_BOOT_COMPLETED` | Re-arm pending reminders after a reboot or app update. | No |
| `RECORD_AUDIO` | Voice-to-text capture and voice-memo attachments. Audio is processed by the on-device speech recognizer (Google's STT, governed by your device's settings) for transcription. Voice-memo attachments are stored locally as audio files. | Speech-to-text routes through your device's configured recognizer; see your system settings for that service's policy. Audio attachments never leave the device. |
| `CAMERA` | Attach freshly taken photos to items. Gallery picks go through the Android system Photo Picker, which exposes only what you select and needs no permission. Photos are copied into the app's private storage. | No |
| `READ_CALENDAR` / `WRITE_CALENDAR` | **Opt-in** two-way sync with your system calendar. Disabled until you turn it on in Settings → Calendar Sync. When enabled, dated items mirror into a Cleartray-owned calendar on your device. | No — only the on-device system calendar is touched. Whether your system calendar itself is synced to Google/Apple/etc. is governed by *your* OS account settings, not Cleartray. |
| `INTERNET` | Declared so optional crash reporting (below) and `url_launcher` can work. The app performs **no network requests on its own** in normal operation. | Only if crash reporting is enabled (see §4) or you tap a link in an item note (which opens your browser, not us). |

## 4. Crash reporting — opt-in, off by default

The app ships with **Sentry** crash reporting integrated, but disabled. The toggle lives in Settings → Privacy (`crash_reporting_enabled`); the default is `false`.

If you turn it on:
- Uncaught crashes and unhandled errors are sent to Sentry (sentry.io, Functional Software Inc.).
- We configure Sentry with `sendDefaultPii = false` and `attachScreenshot = false`. We do not attach your item content, attachments, screenshots, or device identifiers beyond what Sentry collects for stack-trace symbolication (OS version, app version, anonymous install ID).
- A 10% trace sample rate is used to keep volume low.
- You can turn it back off at any time; future crashes stop being sent immediately.

Sentry's own privacy policy: https://sentry.io/privacy/

## 5. What we do *not* do

- We do not show ads.
- We do not run analytics SDKs.
- We do not have user accounts.
- We do not sell, share, rent, or trade any data — there's nothing to sell.
- We do not use your data for advertising, marketing, or any kind of profiling.
- We do not have a Cleartray server. The app does not talk to one.

## 6. Children

Cleartray is rated for general audiences but is not directed at children under 13. We do not knowingly collect data from children (or anyone — see above).

## 7. Changes to this policy

If we change this policy, the new version replaces this file at the same URL and the **Effective date** at the top is updated. Material changes will be noted in the app's release notes.

## 8. Contact

Questions or concerns:

**feipeng@clarifisg.com**

You can also open an issue at the project's source repository.

---

*Cleartray is an independent app. "Getting Things Done" and "GTD" are trademarks of the David Allen Company; Cleartray is not affiliated with, endorsed by, or sponsored by David Allen Company.*
