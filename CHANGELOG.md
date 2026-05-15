# KU Shuttle Change Log

This file records important reasoning, schedule fixes, and website changes before Mindy reviews and approves any GitHub push.

## 2026-05-15 11:32 +04

- Scope: replaced the expired final exam schedule with the regular Spring 2026 daily shuttle schedule.
- Source: `Fifth Update_Daily Shuttle Service Bus Schedule_ Spring 2026.pdf`, saved locally under `bus表/`.
- Reason: KU Student Transportation indicated on 2026-05-15 that students should follow the regular Daily Shuttle Service schedule shared on April 5, 2026.
- Evidence: the April 5 Outlook email `Daily Shuttle Service Resumption – Spring Term 2026` from `StudentTransportation@ku.ac.ae` matched the local PDF by subject/date/attachment keyword/local filename. Exact byte-level attachment hash was not available from the Outlook connector.
- Website change: replaced date-limited exam periods with recurring `Mon-Thu` and `Friday` schedule modes. Saturday and Sunday now show no service unless a user opens all times manually for review.
- UI change: replaced the schedule dropdown with a two-button `Mon-Thu` / `Friday` switch for quicker mobile use.
- Logic fix: added weekday rules for special departures marked `Thursday only`, `Monday & Wednesday only`, and `Tuesday & Thursday only`. The main next-bus card now skips departures that do not run today, while `All departures` keeps them visible but faded with `not today`.
- Wording: kept the footer disclaimer as `Note: this is an unofficial student-made helper.` Added `Regular daily shuttle service is reportedly following the April 5 schedule.` Added `SAN Campus routes include Arzanah where listed in the source schedule.`
- Validation: compared regular PDF pages against key website routes, including dorms to Main, Main to dorms, dorms to SAN, SAN to dorms, Main to SAN, SAN to Main, Masdar to Main, Main to Masdar, Masdar to SAN, SAN to Masdar, and Friday campus routes. The checked routes matched after correcting `SAN Campus -> Masdar` to use only the dedicated Masdar/SAN table.
- Publish status: local draft only. Do not push until Mindy checks the page and explicitly approves.

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
