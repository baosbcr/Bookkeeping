# Weekly Status — DTU Teambuilding

This file accumulates work done during the week for the weekly status update sent to Toke.
**Reset this file after each submission** (delete the bullet points under the current week, keep the header).

---

## Week of 02.06.2026

- Replaced the late-entry checkbox with a 4-option lever (keep / flex / discard-survey-only / discard-all), giving clearer control over whether late-entry students are included or excluded from team formation
- Extended dropped-student detection to also flag group export students absent from the classlist — since the classlist is exported last, absence from it reliably indicates likely withdrawal; the existing dropped lever now applies to both cases
- Added an "audit potentially unenrolled" option to the interactive review, surfacing these students with a clear warning badge
- UI and docs clarity pass: renamed "Lever settings" to "Edge case settings", improved option descriptions, removed internal jargon from user-facing text
- Organised all course run data into separate per-run folders (January 2026, June 2026, August 2025); removed hardcoded default file paths from the CLI so both --surveys and --groups are now required flags; renamed --reports to --surveys throughout for clarity
- Rewrote the README to lead with a complete plain-English guide to the Flask app — every form section explained, all levers described, interactive review flow documented end to end
- Fixed a bug where classlist confirmation was never shown on the interactive review page; redesigned the student ID badges to show "group export" and/or "classlist" in green/blue when the number is reliable, and "Q1 answer" in orange/red only as a last resort; sticky column headers added to both interactive review tables


## Week of 07.06.2026

- Pulled a large update from the Teambuilding repo: course run data reorganised into per-run folders (January 2026, June 2026, August 2025), plus several code and docs improvements from a previous session
- Reviewed and expanded the todo list: added a Q1 `Accept` button for unresolvable students in the interactive review (high priority); added items for missing survey file warnings, Case D opt-in, ghost student informational rows, and log message consistency (all low priority)

- Added a one-click button to the ID review page so auditors can copy a student's survey answer into the student number field without manual copy-paste, useful when verifying non-standard usernames
- Extended the force-audit field to also accept non-standard DTU usernames and emails (e.g. nipac or nipac@dtu.dk), not just standard student numbers
- Added a new teams_overview.csv output file — a compact side-by-side grid showing each challenge's teams with team ID, challenge, and size; the full diversity summary remains unchanged
- Corrected the June course folder name (was mislabelled June 2026); removed unused summary report exports from January 2026; ran both January 2026 and June 2025 pipelines cleanly
- Discovered the June 2025 Challenge A survey file is actually the August 2025 export — confirmed by matching against classlists (100% August, 0% June); correct file needs re-export from DTU Learn
