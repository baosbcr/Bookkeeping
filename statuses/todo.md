## Priority Medium

Investigate the role of the "Target team size" (--ideal) lever — it may be redundant given that --min/--max already bound team size and --max-groups hard-enforces the number of teams per challenge. With a fixed team count and limited students, evenness is largely determined by simple division; the "ideal" target may no longer be pulling its weight as a separate input. If confirmed redundant, remove it from the UI, CLI, and docs. Also rename "Max teams per challenge" to "Teams per challenge" across UI, CLI flags, and docs.

Audit documentation and README for any other ordering inconsistencies — terms, case codes, or concepts referenced before they are defined (the DOCS.md case-code ordering was one example; check that no others remain).

Test and visually inspect the new interactive assignment review mode: run the app with 2026 data, exercise automatic mode (regression), interactive mode (edge cases appear, dropdowns pre-filled), F1 opt-in, force-audit tag input, override a student and verify teams.csv, localStorage persistence, and reset buttons. Also verify the existing ID review flow (`/resolve`) still works end-to-end.
