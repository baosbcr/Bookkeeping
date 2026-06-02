## Priority Medium

Investigate the necessity of the "Target team size" goal — is it pulling its weight given min/max constraints already bound the result? Also rename "Max teams per challenge" to "Teams per challenge" across the UI, CLI flags, and docs.

Test and visually inspect the new interactive assignment review mode: run the app with 2026 data, exercise automatic mode (regression), interactive mode (edge cases appear, dropdowns pre-filled), F1 opt-in, force-audit tag input, override a student and verify teams.csv, localStorage persistence, and reset buttons. Also verify the existing ID review flow (`/resolve`) still works end-to-end.
