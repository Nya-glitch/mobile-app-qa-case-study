# Phase 1: Install, launch, permissions

Date: 2026-11-05 to 2026-11-06
Tester: Esther Nyabate
Device: Redmi A5, Android 15
App version: 0.1.2

| ID | Test | Steps | Expected | Actual | Pass/Fail | Bug ID |
|----|------|-------|----------|--------|-----------|--------|
| 1.1 | Icon and app name | Find the app in the app drawer. Check name, sharpness, logo text, centering. | Name fully visible, icon sharp, all logo text readable, logo centered. | Name, sharpness and centering are fine. Tagline under the logo is too small and low-contrast to read. | Fail (partial) | BUG-001 |
| 1.2 | Cold launch | Close the app from Recents. Start a screen recording. Tap the icon. Wait for the first usable screen. | App opens with no crash or blank screen, in under about 5 seconds. | Opened in about 1.5 seconds. No crash, no blank screen. Splash screen has a typo in the tagline and the logo is cut off at both edges. | Pass (with cosmetic bugs) | BUG-002, BUG-003 |
| 1.3 | Permissions | Settings, Apps, Begah Homes, Permissions. List what is allowed and not allowed. | Only permissions the app needs. App works if denied. | No permissions allowed. Only Notifications listed, under Not allowed. App works normally. Notification prompt timing not observed. | Pass | - |
| 1.4 | Relaunch and background | Press Home, wait 10 seconds, reopen. Repeat with a 2 minute wait. | App resumes where it was. No restart, logout or blank screen. | Resumed on the Portfolio after both waits. | Pass | - |
| 1.5 | Launch with no internet | Close the app. Turn on Airplane mode. Open the app. Then turn Airplane mode off. | Clear message. App recovers when the connection returns. | Clear message shown, no crash. Text says "Tap below to retry" but there is no retry button. Error stays after the connection returns; refresh and tab switching do not clear it. Closing and reopening the app fixes it. | Fail | BUG-004, BUG-005 |
| 1.6 | Back button on first screen | Close the app. Open it. On the first screen, press Back once. | App exits cleanly, no freeze or loop. | App closed. | Pass | - |
| 1.7 | Storage footprint | Settings, Apps, Begah Homes, Storage. Record app size, data and cache. | Reasonable size. Data and cache stay small. | App size 59.70 MB, user data 77.82 kB, cache 193 kB, total 59.97 MB. | Pass (note) | - |

## Evidence
- Test 1.1 / BUG-001: screenshots/P1-1.1-icon.jpg
- Test 1.2 / BUG-002: screenshots/BUG-002-typo-tagline.jpg
- Test 1.2 / BUG-003: screenshots/BUG-003-logo-cut-off.jpg
- Test 1.2 screen recording: kept on the phone
- Test 1.5 / BUG-004: screenshots/BUG-004-no-retry-button.jpg
- Test 1.5 / BUG-005: screenshots/BUG-005-error-persists-after-reconnect.jpg
- Test 1.7: screenshots/P1-1.7-storage.jpg

## Notes
- The logo and icon are being replaced, so further logo and icon checks are out of scope for now.
- Test 1.7: about 60 MB is on the large side for this kind of app. Worth reviewing image and library sizes. Not a bug.
- Test 1.3: notification prompt timing was not observed. Re-check on a fresh install.

## Phase 1 summary
- 7 tests run: 5 passed, 1 partial fail (1.1), 1 fail (1.5).
- 5 bugs logged: BUG-001, BUG-002, BUG-003 (Low), BUG-004 (Medium), BUG-005 (High).