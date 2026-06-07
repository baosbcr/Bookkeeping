## Priority High

Test and visually inspect the full pipeline: run the app with 2026 data and exercise — automatic mode (regression), interactive mode (edge cases appear, dropdowns pre-filled), F1 opt-in, audit_dropped option (with classlist, verify not-in-classlist badge appears), force-audit tag input, override a student and verify teams.csv, all four --late-entries modes (keep/flex/discard-survey-only/discard-all), localStorage persistence and reset buttons, and the existing ID review flow (/resolve). Also verify the new ID confirmation badges: group export (blue) and classlist (green) appear correctly for export students with classlist uploaded; Q1 answer (orange) appears for survey-only students without classlist; sticky headers work in both review tables.

In the interactive assignment review, for unresolvable students that have a Q1 answer available, add a small "Accept" button next to the displayed Q1 answer. Clicking it auto-fills the Q1 value into the student number override text input for that row, saving the auditor from typing it manually. Only shown when Q1 is non-empty and the student is unresolvable (no sXXXXXX recoverable from export or classlist).

## Priority Medium (parked)

Investigate what happens when a ghost student is entered into the force-audit field in interactive mode — ghosts are absent from both the group export and all surveys, so they may not match any student in the pipeline's data. Verify whether the force-audit mechanism handles this gracefully (expected: WARNING [force-audit] no match) or silently does nothing.

Investigate the role of the "Target team size" (--ideal) lever — it may be redundant given that --min/--max already bound team size and --max-groups hard-enforces the number of teams per challenge. With a fixed team count and limited students, evenness is largely determined by simple division; the "ideal" target may no longer be pulling its weight as a separate input. If confirmed redundant, remove it from the UI, CLI, and docs. Also rename "Max teams per challenge" to "Teams per challenge" across UI, CLI flags, and docs.

Audit documentation and README for any other ordering inconsistencies — terms, case codes, or concepts referenced before they are defined (the DOCS.md case-code ordering was one example; check that no others remain).

## Priority Low

Implement multi-file group export support — see PLAN_multi_group_export.md in the Teambuilding repo for the full design (resolve.py, pipeline.py, app.py, index.html changes). Only needed for the August edition of the course. Before running August 2025 data: investigate whether the Overflow group is absent because that run didn't have one, or because the CSV was downloaded before Overflow enrolled.

Investigate what the app does when individual survey files are partially or fully missing — does it warn the auditor that a whole group's survey is absent, or does it silently treat every student in that group as having no survey (Case E)? Should surface a clear warning if an expected survey file (e.g. Challenge B) is not uploaded, so the auditor knows the gap is a missing file rather than a genuine mass non-response.
