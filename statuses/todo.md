## Priority High

Reformulate team formation according to new priority rules.
Number of teams per challenge is defined then after using the overflow and late entries try to achieve similar number of participants across all challenges.

Match new expected output style.

Re-run the pipeline with the full classlist export (not the 50-student sample currently in the repo). Verify dtu_username and email_student_number are populated correctly for the non-standard username students (macoda, alesu, jcoro, kaswu, dovli, xicsu, mpabo, jhaja).

## Priority Medium

Using mock_teams or else as a way to generate mock student data, create deliberate test cases for edge cases and test the resulting output matches expected with various actuation of the levers. Make the tests digestible to human audit by keeping the number of teams 3-4 for each challenge at most. Document clearly — this is where I will audit the results.
