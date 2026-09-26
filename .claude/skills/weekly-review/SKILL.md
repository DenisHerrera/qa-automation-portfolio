---
name: weekly-review
description: Review Denis's weekly study-plan deliverable like a senior QA code review, score it with the 5-criteria rubric, quiz him on the concepts and update PROGRESS.md. Use when Denis asks to review, grade or close a week (e.g. "revisa la semana 3").
---

# Weekly review

Run this when Denis asks to review a week of his 12-week QA Automation plan.

## Steps

1. Identify the week number and read its row in `PROGRESS.md`.
2. Look at the changes for that week (`git log` and `git diff` since the previous review entry).
3. Run the relevant tests locally and check the latest GitHub Actions run if available.
4. Review the code against the standards in `CLAUDE.md`.
5. Score each criterion from 1 to 5, with one sentence of evidence each:
   - Works: tests pass and the pipeline is green.
   - Code quality: SOLID, readability, no duplication, no hard-coded waits.
   - Test design / coverage: uses techniques such as equivalence partitioning, boundary values,
     negative cases; tests are independent.
   - Documentation: clear README in English, explains how to run and what was learned.
   - Defense: ask Denis 3 "why" questions about his decisions and score his answers.
6. Give the 3 most important improvements, ordered by impact. Hints only; do not rewrite his code
   unless he asks for the solution.
7. Ask 5 short concept questions about the week's topics (one at a time) and record the score.
8. Update `PROGRESS.md`: status, average score, quiz result, and a new entry in "Review details".
9. A week is "Done" only if every criterion is 3/5 or higher. Otherwise mark it "Needs rework"
   and list what to fix.

## Tone

Honest and specific, like a senior teammate. Praise what is genuinely good, be direct about gaps.
Answer in Spanish; keep code and file contents in English.
