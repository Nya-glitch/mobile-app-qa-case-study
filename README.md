# Mobile App QA Case Study

A manual QA case study on an Android property-management app ((Begah Homes, shared with the developer's permission)). It covers test planning, test execution, bug reporting and usability review.

## What I did
- Wrote a test plan covering 11 phases, with a severity guide
- Executed 18 tests across app launch and login, and logged every result
- Reported 5 bugs, each with steps to reproduce, expected and actual results, severity and evidence
- Recorded 5 usability notes that are not bugs but would improve the app

## Highlights
- **BUG-005 (High):** the app stays stuck on "Cannot reach the server" after the connection returns; only a full restart recovers it
- **BUG-004 (Medium):** the screen says "Tap below to retry" but there is no retry button
- 13 of the 18 tests passed with no issues

## Test environment
- Device: Redmi A5, Android 15
- App version: 0.1.2
- Test dates: 2026-11-05 to 2026-11-06

## Structure
- `test-plan.md`: phases and severity guide
- `test-log/`: results per phase
- `bugs/`: one file per bug
- `screenshots/`: evidence, with sensitive details hidden
- `usability-notes.md`: non-bug improvement suggestions

## Tools
Manual testing on a real device, Markdown for documentation, Git and GitHub for version control.