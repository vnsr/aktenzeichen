# Aktenzeichen – deadlines, contracts & documents (offline PWA)

Tracks one-off deadlines, contracts with notice periods, expiring documents and recurring tasks, and warns you in time.
Your data stays on the phone. Nothing is sent anywhere unless you turn on automatic sync to your own private GitHub repository.

## Install (once)
1. Repo → **Settings → Pages** → Source "Deploy from a branch", branch `main`, folder `/ (root)` → Save.
2. After about a minute, open **https://vnsr.github.io/aktenzeichen/** in **Safari** on the iPhone → Share → **Add to Home Screen**.
3. Open it once from the icon while online. After that it works offline.

## What it does
- **Upcoming:** everything that needs action, grouped Overdue → Act now (inside the warning time) → Next 30 days → Later this year.
- **Contracts:** enter the start date, minimum term, renewal period and notice period; Aktenzeichen works out the next *cancel by* date and the end date it leads to. Contracts that can be cancelled any month stay off the Upcoming list. Monthly and yearly cost totals by category.
  **Write cancellation** makes a German Kündigung letter (copy or share), **Mark as cancelled** tracks the end date.
- **Documents:** expiry dates per person, with a renewal lead time (e.g. 120 days for a passport). **Renewed** sets the new date and keeps the old one in the notes.
- **Deadlines & recurring:** one-off dates, and things like HU/TÜV, Reifenwechsel or Steuererklärung that roll forward when you tap **Done**.
- **Attachments:** photos (shrunk to ~2000 px) or PDFs up to 15 MB per item.
- **Calendar:** **Add to Calendar** on any item, or Settings → **Export to Calendar** for everything upcoming. This is a one-off .ics import with alarms; export again after changes.

Presets fill in typical values (e.g. Kfz-Versicherung: renews yearly, one month's notice → cancel by 30 Nov). They are not legal advice: check your contract.

## Automatic sync
Same setup as Yupu and Thali: Settings → Automatic sync → `username/my-app-data` and the phone's existing token.
Aktenzeichen writes only to `aktenzeichen/` (`aktenzeichen/items.json`, attachments in `aktenzeichen/files/`).
Your name and address for letters stay on the phone and are not synced.

## Backups
Settings → **Back up to Files** (items only; attachments are in the sync repository). **Import backup** merges.

## v1.0.0 (15 Oct 2026)
First version.

## v1.0.1 (15 Oct 2026)
The header and bottom bar stay fixed while scrolling on iPhone; only the content area scrolls.

## v1.0.2 (16 Oct 2026)
Placeholders and examples use neutral names.

## v1.1.0 (16 Oct 2026)
New look: a dark "HUD" console design.
- **Radar** on Upcoming: every date is a blip. Distance from the centre is days left (rings at 7, 30, 90 days and 1 year), the sector is the type of item. Amber blips need action now, red ones are overdue; tap one to open it.
- **Case numbers**: every item gets its own reference, e.g. `AZ-V-26-0473` (V contract, D document, F deadline, W recurring).
- **T-minus countdown**: `T−16` means 16 days left, `T+2` two days late. The item view shows a large countdown.
- Colours carry meaning: cyan on track, amber act now, red overdue. The app now always uses the dark design.
- Typeface Chakra Petch is bundled in `fonts/` (SIL Open Font License), so it works offline.

