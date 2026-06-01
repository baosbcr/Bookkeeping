## Priority Medium

Investigate the necessity of the "Target team size" goal — is it pulling its weight given min/max constraints already bound the result? Also rename "Max teams per challenge" to "Teams per challenge" across the UI, CLI flags, and docs.

Create an interactive resolution step for challenge assignment edge cases (cross-challenge surveys, multiple surveys, etc.). This runs before overflow/late-entry normalisation and before team formation — its sole purpose is locking each student to the right challenge (or moving them to overflow). Modelled after the existing student-number interactive review.
