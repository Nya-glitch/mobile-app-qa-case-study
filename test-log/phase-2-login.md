# Phase 2: Login

Date: 2026-11-06
Tester: Esther Nyabate
Device: Redmi A5, Android 15
App version: 0.1.2

| ID | Test | Steps | Expected | Actual | Pass/Fail | Bug ID |
|----|------|-------|----------|--------|-----------|--------|
| 2.1 | Valid login | Enter correct property code, email and password. Tap Sign In. | Reaches Portfolio screen quickly. | Reached Portfolio in about 2 seconds. | Pass | - |
| 2.2 | Wrong password | Enter correct details with a wrong password. | Login refused with a clear message. | "Invalid Credentials" shown. No crash. | Pass | - |
| 2.3 | Empty fields | Tap Sign In with empty fields, one at a time. | Clear required-field messages. | "Enter your email or phone number" and "Enter your password" shown. Property Code accepted empty. | Pass | - |
| 2.4 | Invalid email format | Try abc, abc@ and abc@gmail with a password. | Clear message, no crash. | "Invalid Credentials" shown each time. No app-side format check. | Pass (note) | - |
| 2.5 | Password field | Type a password and tap the eye icon. | Hidden by default, eye icon toggles. | Dots by default, eye icon works. | Pass | - |
| 2.6 | Session after restart | Log in, close app from Recents, reopen. | Defined behaviour. | Goes straight to Portfolio. | Pass | - |
| 2.7 | Logout and Back button | Tap logout, then press Back. | Returns to login. Back must not reopen the Portfolio. | Logs out at once, no confirmation. Back closes the app. | Pass | - |
| 2.8 | Saved details after logout | Log in, log out, look at the login screen. | Defined behaviour. | All fields come back empty. No "Remember me" option. Google offered to save the password. | Pass (note) | - |
| 2.9 | Double-tap Sign In | Enter correct details. Tap Sign In twice quickly. | Opens the Portfolio once, no errors. | Portfolio opened once. No abnormal behaviour. | Pass | - |
| 2.10 | Login with no internet | Turn on Airplane mode. Enter correct details. Tap Sign In. | Clear message, no crash or endless spinner. | "Cannot reach the server. Check your connection." Fields keep what was typed. | Pass | - |
| 2.11 | Very long email | Enter an email of about 100 characters with a password. Tap Sign In. | Layout holds, clear message, no crash. | Layout intact. "Invalid Credentials" shown. No crash. | Pass | - |

## Notes
- Helper text under Property Code and the email placeholder are cut off with an ellipsis. Not a bug; recorded as UX-001 in usability-notes.md.
- No logout confirmation: recorded as UX-002.
- No email format check on the app side: recorded as UX-003.
- Details must be retyped after every logout: to be recorded as UX-004.
- No "Forgot password" or "Sign up" link on the login screen: to be recorded as UX-005.
- Screenshots containing real credentials were not saved to the repo.