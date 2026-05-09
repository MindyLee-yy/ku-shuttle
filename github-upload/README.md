# KU Shuttle

Lightweight static shuttle timetable for Khalifa University.

## Weekly update

When a new transportation PDF or Excel file arrives, put it in `sources/` locally, then run:

```bash
python3 scripts/update_schedule.py "sources/new-schedule.xlsx"
```

The script updates:

- `data/schedule-current.json`
- the embedded schedule data inside `index.html`

Then commit and push to GitHub Pages. The public link stays the same.

## Notes

- `sources/` is ignored by Git so original email attachments stay local.
- `index.html` is the current public page.
- `index-v1.html`, `index-v2.html`, and `index-v3.html` are local archived prototypes.
