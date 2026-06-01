# DTU IE Bookkeeping — Project Context for Claude

## Purpose

Administrative tracking for João's DTU IE student assistant position (DTU Teambuilding project, supervisor: Toke). Entirely separate from the team formation tool repo (baosbcr/Teambuilding).

Contains two things:
1. **Task list & status messages** — running task list and weekly status drafts for Toke
2. **Hours log** — monthly log of hours worked with evidence

---

## Directory Layout

```
Bookkeeping/
├── CLAUDE.md                  ← this file
├── agendas/                   ← monthly agenda PDF exports from Outlook
│   └── 2026-05-may.pdf
├── hours/
│   ├── 2026-05-may.md         ← per-month hours table
│   ├── 2026-06-june.md
│   └── monthly_summary.md     ← running total across all months
└── statuses/
    ├── todo.md                ← task list and priorities
    └── weekly_status.md       ← draft for weekly update to Toke
```

---

## Hours Log

Monthly files live at `hours/YYYY-MM-month.md`. Each file has a running total at the top and a table:

```markdown
**Total: X.X h**

| Date | Hours | Evidence | Notes |
|------|-------|----------|-------|
| 2026-05-27 | 3.0 | commits 85138a1–fad7632 (Teambuilding repo) | dtu_username + enrichment |
```

**Rules:**
- Place hours on the days work actually happened, not a preferred schedule.
- Before logging a day, check the relevant agenda file in `agendas/` for meetings with Toke or Alexander — count those and note them in Evidence.
- If a meeting ran over and there's commit activity after it, credit the extra time.
- Exam periods: flag weeks with a note, reduce hours.
- Never inflate. If evidence is thin, keep estimate conservative and say so.
- At month end, produce a clean summary table ready to paste into the timesheet form.

After each working session, append a row to the current month's file.

---

## Status Messages

### `statuses/weekly_status.md`

Running log of work done each week, used to draft the weekly update sent to Toke. Written as if the reader has seen the Flask app run once or twice — no internal jargon.

Append to it at the end of every working session. After the user confirms they've submitted the update, clear the bullet points under the current week heading and start fresh.

### `statuses/todo.md`

Prioritised task list. Keep it current — mark items done and remove them when no longer relevant.

---

## Project Repos

- Team formation tool: `baosbcr/Teambuilding` (separate repo, do not mix)
- This bookkeeping repo: `baosbcr/Bookkeeping`
