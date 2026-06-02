# Weekly Status — DTU Teambuilding

This file accumulates work done during the week for the weekly status update sent to Toke.
**Reset this file after each submission** (delete the bullet points under the current week, keep the header).

---

## Week of 02.06.2026

- The interactive student-number review page now shows stacked colour-coded source badges for each student — auditors can see at a glance how many independent sources (group export email, classlist email, survey) agree on a student number, making it easy to spot cases that are confirmed by only one system
- Added a "Survey answer" column to the review page showing exactly what the student typed in Q1, and fixed a bug where the classlist confirmation wasn't being carried through correctly
- Added a "New run" button to the review page and made it possible to correct a value and re-download without re-running the full pipeline
- Built a new interactive challenge assignment review step that runs before team formation — when enabled, the app shows every student whose group assignment was ambiguous (wrong-challenge survey, no survey, survey-only student, etc.) with all relevant context and a dropdown pre-filled with the automatic suggestion; the auditor can confirm or override each assignment before teams are formed
- All possible assignments (all four challenges, overflow, late entry, skip) are always available in the dropdown because the auditor may have direct contact or teacher information the system can't see; specific students can also be flagged by ID or email to always appear in the review
- All form settings (mode, levers, audit options) are now saved in the browser and restored automatically on the next visit, with per-section reset buttons
