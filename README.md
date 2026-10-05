# bijli-data

Live data file for the **Bijli Bill Calculator** Android app (Khyber Digital).

- `tariff.json`: domestic electricity slab rates and announcements read by the app.
- The app checks this file about every 12 hours and notifies users when `version` changes or a new item is added at the top of `announcements`.

## Rules for editing `tariff.json`
1. Change slab rates only from an official NEPRA decision or Government notification (SRO).
2. When rates change, update `version` (e.g. the SRO number) and `updated` (YYYY-MM-DD).
3. To send an alert, add a new item at the **top** of `announcements` with a new unique `id`.
4. Keep the file valid JSON. Keep at most 10 announcements.
