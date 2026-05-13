# KU Shuttle Change Log

This file records important reasoning, schedule fixes, and website changes before Mindy reviews and approves any GitHub push.

## 2026-05-13 13:58 +04

- Scope: checked only the `11 to 14 May 2026` sheet from `Final Exam Bus Schedule_Friday 08 May to Thursday 14 May 2026.xlsx`.
- Issue: `Main Campus -> SAN Campus` was incomplete because the Excel schedule lists this route in two different blocks:
  - `From Main Campus to Student Hostels & SAN`
  - `From Student Hostels & Main Campus to SAN`
- Decision: for `Main Campus <-> SAN Campus`, merge both relevant route contexts and deduplicate repeated times instead of choosing only one context.
- Expected `Main Campus -> SAN Campus` times for `11 to 14 May 2026`: `8:00 AM`, `10:00 AM`, `11:30 AM`, `12:00 PM`, `1:00 PM`, `3:00 PM`, `3:30 PM`, `6:30 PM`, `7:00 PM`, `7:30 PM`, `8:00 PM`.
- Website change: updated `index.html` so `main>san` and `san>main` keep all merged campus-to-campus departures.
- Public wording: added a small footer disclaimer, `Note: this is an unofficial student-made helper.`
- Footer metadata: changed the displayed schedule range to `Monday 11 May to Thursday 14 May 2026` and `Last updated` to `2026-05-13`.
- Validation: compared all 20 website routes for the `11 May - 14 May` period against the `11 to 14 May 2026` Excel sheet. All expected times matched, including the merged `Main Campus -> SAN Campus` route.
- Publish status: local draft only. Do not push until Mindy checks the page and explicitly approves.
